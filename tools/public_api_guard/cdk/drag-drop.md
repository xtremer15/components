## API Report File for "components-srcs"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AfterViewInit } from '@angular/core';
import { BooleanInput } from '@angular/cdk/coercion';
import { ChangeDetectorRef } from '@angular/core';
import { Direction } from '@angular/cdk/bidi';
import { Directionality } from '@angular/cdk/bidi';
import { ElementRef } from '@angular/core';
import { EventEmitter } from '@angular/core';
import * as i0 from '@angular/core';
import * as i7 from '@angular/cdk/scrolling';
import { InjectionToken } from '@angular/core';
import { NgZone } from '@angular/core';
import { NumberInput } from '@angular/cdk/coercion';
import { Observable } from 'rxjs';
import { OnChanges } from '@angular/core';
import { OnDestroy } from '@angular/core';
import { QueryList } from '@angular/core';
import { ScrollDispatcher } from '@angular/cdk/scrolling';
import { SimpleChanges } from '@angular/core';
import { Subject } from 'rxjs';
import { TemplateRef } from '@angular/core';
import { ViewContainerRef } from '@angular/core';
import { ViewportRuler } from '@angular/cdk/scrolling';

// @public
export const CDK_DRAG_CONFIG: InjectionToken<DragDropConfig>;

// @public
export const CDK_DRAG_HANDLE: InjectionToken<CdkDragHandle>;

// @public
export const CDK_DRAG_PARENT: InjectionToken<{}>;

// @public
export const CDK_DRAG_PLACEHOLDER: InjectionToken<CdkDragPlaceholder<any>>;

// @public
export const CDK_DRAG_PREVIEW: InjectionToken<CdkDragPreview<any>>;

// @public
export const CDK_DROP_LIST: InjectionToken<CdkDropList<any>>;

// @public
export const CDK_DROP_LIST_GROUP: InjectionToken<CdkDropListGroup<unknown>>;

// @public
export class CdkDrag<T = any> implements AfterViewInit, OnChanges, OnDestroy {
    constructor(
    element: ElementRef<HTMLElement>,
    dropContainer: CdkDropListInternal,
    _document: any, _ngZone: NgZone, _viewContainerRef: ViewContainerRef, config: DragDropConfig, _dir: Directionality, dragDrop: DragDrop, _changeDetectorRef: ChangeDetectorRef, _selfHandle?: CdkDragHandle | undefined, _parentDrag?: CdkDrag<any> | undefined);
    boundaryElement: string | ElementRef<HTMLElement> | HTMLElement;
    constrainPosition?: (userPointerPosition: Point, dragRef: DragRef, dimensions: ClientRect, pickupPositionInElement: Point) => Point;
    data: T;
    get disabled(): boolean;
    set disabled(value: BooleanInput);
    _dragRef: DragRef<CdkDrag<T>>;
    dragStartDelay: DragStartDelay;
    dropContainer: CdkDropListInternal;
    readonly dropped: EventEmitter<CdkDragDrop<any>>;
    element: ElementRef<HTMLElement>;
    readonly ended: EventEmitter<CdkDragEnd>;
    readonly entered: EventEmitter<CdkDragEnter<any>>;
    readonly exited: EventEmitter<CdkDragExit<any>>;
    freeDragPosition: Point;
    getFreeDragPosition(): Readonly<Point>;
    getPlaceholderElement(): HTMLElement;
    getRootElement(): HTMLElement;
    _handles: QueryList<CdkDragHandle>;
    lockAxis: DragAxis;
    readonly moved: Observable<CdkDragMove<T>>;
    // (undocumented)
    ngAfterViewInit(): void;
    // (undocumented)
    ngOnChanges(changes: SimpleChanges): void;
    // (undocumented)
    ngOnDestroy(): void;
    _placeholderTemplate: CdkDragPlaceholder;
    previewClass: string | string[];
    previewContainer: PreviewContainer;
    _previewTemplate: CdkDragPreview;
    readonly released: EventEmitter<CdkDragRelease>;
    reset(): void;
    rootElementSelector: string;
    setFreeDragPosition(value: Point): void;
    readonly started: EventEmitter<CdkDragStart>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDrag<any>, "[cdkDrag]", ["cdkDrag"], { "data": "cdkDragData"; "lockAxis": "cdkDragLockAxis"; "rootElementSelector": "cdkDragRootElement"; "boundaryElement": "cdkDragBoundary"; "dragStartDelay": "cdkDragStartDelay"; "freeDragPosition": "cdkDragFreeDragPosition"; "disabled": "cdkDragDisabled"; "constrainPosition": "cdkDragConstrainPosition"; "previewClass": "cdkDragPreviewClass"; "previewContainer": "cdkDragPreviewContainer"; }, { "started": "cdkDragStarted"; "released": "cdkDragReleased"; "ended": "cdkDragEnded"; "entered": "cdkDragEntered"; "exited": "cdkDragExited"; "dropped": "cdkDragDropped"; "moved": "cdkDragMoved"; }, ["_previewTemplate", "_placeholderTemplate", "_handles"], never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDrag<any>, [null, { optional: true; skipSelf: true; }, null, null, null, { optional: true; }, { optional: true; }, null, null, { optional: true; self: true; }, { optional: true; skipSelf: true; }]>;
}

// @public
export interface CdkDragDrop<T, O = T, I = any> {
    container: CdkDropList<T>;
    currentIndex: number;
    distance: {
        x: number;
        y: number;
    };
    dropPoint: {
        x: number;
        y: number;
    };
    event: MouseEvent | TouchEvent;
    isPointerOverContainer: boolean;
    item: CdkDrag<I>;
    previousContainer: CdkDropList<O>;
    previousIndex: number;
}

// @public
export interface CdkDragEnd<T = any> {
    distance: {
        x: number;
        y: number;
    };
    dropPoint: {
        x: number;
        y: number;
    };
    event: MouseEvent | TouchEvent;
    source: CdkDrag<T>;
}

// @public
export interface CdkDragEnter<T = any, I = T> {
    container: CdkDropList<T>;
    currentIndex: number;
    item: CdkDrag<I>;
}

// @public
export interface CdkDragExit<T = any, I = T> {
    container: CdkDropList<T>;
    item: CdkDrag<I>;
}

// @public
export class CdkDragHandle implements OnDestroy {
    constructor(element: ElementRef<HTMLElement>, parentDrag?: any);
    get disabled(): boolean;
    set disabled(value: BooleanInput);
    // (undocumented)
    element: ElementRef<HTMLElement>;
    // (undocumented)
    ngOnDestroy(): void;
    _parentDrag: {} | undefined;
    readonly _stateChanges: Subject<CdkDragHandle>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDragHandle, "[cdkDragHandle]", never, { "disabled": "cdkDragHandleDisabled"; }, {}, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDragHandle, [null, { optional: true; skipSelf: true; }]>;
}

// @public
export interface CdkDragMove<T = any> {
    delta: {
        x: -1 | 0 | 1;
        y: -1 | 0 | 1;
    };
    distance: {
        x: number;
        y: number;
    };
    event: MouseEvent | TouchEvent;
    pointerPosition: {
        x: number;
        y: number;
    };
    source: CdkDrag<T>;
}

// @public
export class CdkDragPlaceholder<T = any> {
    constructor(templateRef: TemplateRef<T>);
    data: T;
    // (undocumented)
    templateRef: TemplateRef<T>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDragPlaceholder<any>, "ng-template[cdkDragPlaceholder]", never, { "data": "data"; }, {}, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDragPlaceholder<any>, never>;
}

// @public
export class CdkDragPreview<T = any> {
    constructor(templateRef: TemplateRef<T>);
    data: T;
    get matchSize(): boolean;
    set matchSize(value: BooleanInput);
    // (undocumented)
    templateRef: TemplateRef<T>;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDragPreview<any>, "ng-template[cdkDragPreview]", never, { "data": "data"; "matchSize": "matchSize"; }, {}, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDragPreview<any>, never>;
}

// @public
export interface CdkDragRelease<T = any> {
    event: MouseEvent | TouchEvent;
    source: CdkDrag<T>;
}

// @public
export interface CdkDragSortEvent<T = any, I = T> {
    container: CdkDropList<T>;
    currentIndex: number;
    item: CdkDrag<I>;
    previousIndex: number;
}

// @public
export interface CdkDragStart<T = any> {
    event: MouseEvent | TouchEvent;
    source: CdkDrag<T>;
}

// @public
export class CdkDropList<T = any> implements OnDestroy {
    constructor(
    element: ElementRef<HTMLElement>, dragDrop: DragDrop, _changeDetectorRef: ChangeDetectorRef, _scrollDispatcher: ScrollDispatcher, _dir?: Directionality | undefined, _group?: CdkDropListGroup<CdkDropList<any>> | undefined, config?: DragDropConfig);
    addItem(item: CdkDrag): void;
    autoScrollDisabled: BooleanInput;
    autoScrollStep: NumberInput;
    connectedTo: (CdkDropList | string)[] | CdkDropList | string;
    data: T;
    get disabled(): boolean;
    set disabled(value: BooleanInput);
    _dropListRef: DropListRef<CdkDropList<T>>;
    readonly dropped: EventEmitter<CdkDragDrop<T, any>>;
    element: ElementRef<HTMLElement>;
    readonly entered: EventEmitter<CdkDragEnter<T>>;
    enterPredicate: (drag: CdkDrag, drop: CdkDropList) => boolean;
    readonly exited: EventEmitter<CdkDragExit<T>>;
    getSortedItems(): CdkDrag[];
    id: string;
    lockAxis: DragAxis;
    // (undocumented)
    ngOnDestroy(): void;
    orientation: DropListOrientation;
    removeItem(item: CdkDrag): void;
    readonly sorted: EventEmitter<CdkDragSortEvent<T>>;
    sortingDisabled: BooleanInput;
    sortPredicate: (index: number, drag: CdkDrag, drop: CdkDropList) => boolean;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDropList<any>, "[cdkDropList], cdk-drop-list", ["cdkDropList"], { "connectedTo": "cdkDropListConnectedTo"; "data": "cdkDropListData"; "orientation": "cdkDropListOrientation"; "id": "id"; "lockAxis": "cdkDropListLockAxis"; "disabled": "cdkDropListDisabled"; "sortingDisabled": "cdkDropListSortingDisabled"; "enterPredicate": "cdkDropListEnterPredicate"; "sortPredicate": "cdkDropListSortPredicate"; "autoScrollDisabled": "cdkDropListAutoScrollDisabled"; "autoScrollStep": "cdkDropListAutoScrollStep"; }, { "dropped": "cdkDropListDropped"; "entered": "cdkDropListEntered"; "exited": "cdkDropListExited"; "sorted": "cdkDropListSorted"; }, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDropList<any>, [null, null, null, null, { optional: true; }, { optional: true; skipSelf: true; }, { optional: true; }]>;
}

// @public
export class CdkDropListGroup<T> implements OnDestroy {
    get disabled(): boolean;
    set disabled(value: BooleanInput);
    readonly _items: Set<T>;
    // (undocumented)
    ngOnDestroy(): void;
    // (undocumented)
    static ɵdir: i0.ɵɵDirectiveDeclaration<CdkDropListGroup<any>, "[cdkDropListGroup]", ["cdkDropListGroup"], { "disabled": "cdkDropListGroupDisabled"; }, {}, never, never, true, never>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<CdkDropListGroup<any>, never>;
}

// @public
export function copyArrayItem<T = any>(currentArray: T[], targetArray: T[], currentIndex: number, targetIndex: number): void;

// @public
export type DragAxis = 'x' | 'y';

// @public
export type DragConstrainPosition = (point: Point, dragRef: DragRef) => Point;

// @public
export class DragDrop {
    constructor(_document: any, _ngZone: NgZone, _viewportRuler: ViewportRuler, _dragDropRegistry: DragDropRegistry<DragRef, DropListRef>);
    createDrag<T = any>(element: ElementRef<HTMLElement> | HTMLElement, config?: DragRefConfig): DragRef<T>;
    createDropList<T = any>(element: ElementRef<HTMLElement> | HTMLElement): DropListRef<T>;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<DragDrop, never>;
    // (undocumented)
    static ɵprov: i0.ɵɵInjectableDeclaration<DragDrop>;
}

// @public
export interface DragDropConfig extends Partial<DragRefConfig> {
    // (undocumented)
    boundaryElement?: string;
    // (undocumented)
    constrainPosition?: DragConstrainPosition;
    // (undocumented)
    draggingDisabled?: boolean;
    // (undocumented)
    dragStartDelay?: DragStartDelay;
    // (undocumented)
    listAutoScrollDisabled?: boolean;
    // (undocumented)
    listOrientation?: DropListOrientation;
    // (undocumented)
    lockAxis?: DragAxis;
    // (undocumented)
    previewClass?: string | string[];
    // (undocumented)
    previewContainer?: 'global' | 'parent';
    // (undocumented)
    rootElementSelector?: string;
    // (undocumented)
    sortingDisabled?: boolean;
    // (undocumented)
    zIndex?: number;
}

// @public (undocumented)
export class DragDropModule {
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<DragDropModule, never>;
    // (undocumented)
    static ɵinj: i0.ɵɵInjectorDeclaration<DragDropModule>;
    // (undocumented)
    static ɵmod: i0.ɵɵNgModuleDeclaration<DragDropModule, never, [typeof i1.CdkDropList, typeof i2.CdkDropListGroup, typeof i3.CdkDrag, typeof i4.CdkDragHandle, typeof i5.CdkDragPreview, typeof i6.CdkDragPlaceholder], [typeof i7.CdkScrollableModule, typeof i1.CdkDropList, typeof i2.CdkDropListGroup, typeof i3.CdkDrag, typeof i4.CdkDragHandle, typeof i5.CdkDragPreview, typeof i6.CdkDragPlaceholder]>;
}

// @public
export class DragDropRegistry<I extends {
    isDragging(): boolean;
}, C> implements OnDestroy {
    constructor(_ngZone: NgZone, _document: any);
    isDragging(drag: I): boolean;
    // (undocumented)
    ngOnDestroy(): void;
    readonly pointerMove: Subject<TouchEvent | MouseEvent>;
    readonly pointerUp: Subject<TouchEvent | MouseEvent>;
    registerDragItem(drag: I): void;
    registerDropContainer(drop: C): void;
    removeDragItem(drag: I): void;
    removeDropContainer(drop: C): void;
    // @deprecated
    readonly scroll: Subject<Event>;
    scrolled(shadowRoot?: DocumentOrShadowRoot | null): Observable<Event>;
    startDragging(drag: I, event: TouchEvent | MouseEvent): void;
    stopDragging(drag: I): void;
    // (undocumented)
    static ɵfac: i0.ɵɵFactoryDeclaration<DragDropRegistry<any, any>, never>;
    // (undocumented)
    static ɵprov: i0.ɵɵInjectableDeclaration<DragDropRegistry<any, any>>;
}

// @public
export class DragRef<T = any> {
    constructor(element: ElementRef<HTMLElement> | HTMLElement, _config: DragRefConfig, _document: Document, _ngZone: NgZone, _viewportRuler: ViewportRuler, _dragDropRegistry: DragDropRegistry<DragRef, DropListRefInternal>);
    readonly beforeStarted: Subject<void>;
    constrainPosition?: (userPointerPosition: Point, dragRef: DragRef, dimensions: ClientRect, pickupPositionInElement: Point) => Point;
    data: T;
    get disabled(): boolean;
    set disabled(value: boolean);
    disableHandle(handle: HTMLElement): void;
    dispose(): void;
    dragStartDelay: number | {
        touch: number;
        mouse: number;
    };
    readonly dropped: Subject<{
        previousIndex: number;
        currentIndex: number;
        item: DragRef;
        container: DropListRefInternal;
        previousContainer: DropListRefInternal;
        distance: Point;
        dropPoint: Point;
        isPointerOverContainer: boolean;
        event: MouseEvent | TouchEvent;
    }>;
    enableHandle(handle: HTMLElement): void;
    readonly ended: Subject<{
        source: DragRef;
        distance: Point;
        dropPoint: Point;
        event: MouseEvent | TouchEvent;
    }>;
    readonly entered: Subject<{
        container: DropListRefInternal;
        item: DragRef;
        currentIndex: number;
    }>;
    readonly exited: Subject<{
        container: DropListRefInternal;
        item: DragRef;
    }>;
    getFreeDragPosition(): Readonly<Point>;
    getPlaceholderElement(): HTMLElement;
    getRootElement(): HTMLElement;
    getVisibleElement(): HTMLElement;
    isDragging(): boolean;
    lockAxis: 'x' | 'y';
    readonly moved: Observable<{
        source: DragRef;
        pointerPosition: {
            x: number;
            y: number;
        };
        event: MouseEvent | TouchEvent;
        distance: Point;
        delta: {
            x: -1 | 0 | 1;
            y: -1 | 0 | 1;
        };
    }>;
    previewClass: string | string[] | undefined;
    readonly released: Subject<{
        source: DragRef;
        event: MouseEvent | TouchEvent;
    }>;
    reset(): void;
    setFreeDragPosition(value: Point): this;
    _sortFromLastPointerPosition(): void;
    readonly started: Subject<{
        source: DragRef;
        event: MouseEvent | TouchEvent;
    }>;
    withBoundaryElement(boundaryElement: ElementRef<HTMLElement> | HTMLElement | null): this;
    withDirection(direction: Direction): this;
    _withDropContainer(container: DropListRefInternal): void;
    withHandles(handles: (HTMLElement | ElementRef<HTMLElement>)[]): this;
    withParent(parent: DragRef<unknown> | null): this;
    withPlaceholderTemplate(template: DragHelperTemplate | null): this;
    withPreviewContainer(value: PreviewContainer): this;
    withPreviewTemplate(template: DragPreviewTemplate | null): this;
    withRootElement(rootElement: ElementRef<HTMLElement> | HTMLElement): this;
}

// @public
export interface DragRefConfig {
    dragStartThreshold: number;
    parentDragRef?: DragRef;
    pointerDirectionChangeThreshold: number;
    zIndex?: number;
}

// @public
export type DragStartDelay = number | {
    touch: number;
    mouse: number;
};

// @public
export type DropListOrientation = 'horizontal' | 'vertical';

// @public
export class DropListRef<T = any> {
    constructor(element: ElementRef<HTMLElement> | HTMLElement, _dragDropRegistry: DragDropRegistry<DragRefInternal, DropListRef>, _document: any, _ngZone: NgZone, _viewportRuler: ViewportRuler);
    autoScrollDisabled: boolean;
    autoScrollStep: number;
    readonly beforeStarted: Subject<void>;
    _canReceive(item: DragRefInternal, x: number, y: number): boolean;
    connectedTo(connectedTo: DropListRef[]): this;
    data: T;
    disabled: boolean;
    dispose(): void;
    drop(item: DragRefInternal, currentIndex: number, previousIndex: number, previousContainer: DropListRef, isPointerOverContainer: boolean, distance: Point, dropPoint: Point, event?: MouseEvent | TouchEvent): void;
    readonly dropped: Subject<{
        item: DragRefInternal;
        currentIndex: number;
        previousIndex: number;
        container: DropListRef;
        previousContainer: DropListRef;
        isPointerOverContainer: boolean;
        distance: Point;
        dropPoint: Point;
        event: MouseEvent | TouchEvent;
    }>;
    element: HTMLElement | ElementRef<HTMLElement>;
    enter(item: DragRefInternal, pointerX: number, pointerY: number, index?: number): void;
    readonly entered: Subject<{
        item: DragRefInternal;
        container: DropListRef;
        currentIndex: number;
    }>;
    enterPredicate: (drag: DragRefInternal, drop: DropListRef) => boolean;
    exit(item: DragRefInternal): void;
    readonly exited: Subject<{
        item: DragRefInternal;
        container: DropListRef;
    }>;
    getItemIndex(item: DragRefInternal): number;
    getScrollableParents(): readonly HTMLElement[];
    _getSiblingContainerFromPosition(item: DragRefInternal, x: number, y: number): DropListRef | undefined;
    isDragging(): boolean;
    _isOverContainer(x: number, y: number): boolean;
    isReceiving(): boolean;
    lockAxis: 'x' | 'y';
    readonly sorted: Subject<{
        previousIndex: number;
        currentIndex: number;
        container: DropListRef;
        item: DragRefInternal;
    }>;
    sortingDisabled: boolean;
    _sortItem(item: DragRefInternal, pointerX: number, pointerY: number, pointerDelta: {
        x: number;
        y: number;
    }): void;
    sortPredicate: (index: number, drag: DragRefInternal, drop: DropListRef) => boolean;
    start(): void;
    _startReceiving(sibling: DropListRef, items: DragRefInternal[]): void;
    _startScrollingIfNecessary(pointerX: number, pointerY: number): void;
    _stopReceiving(sibling: DropListRef): void;
    _stopScrolling(): void;
    withDirection(direction: Direction): this;
    withItems(items: DragRefInternal[]): this;
    withOrientation(orientation: 'vertical' | 'horizontal'): this;
    withScrollableParents(elements: HTMLElement[]): this;
}

// @public
export function moveItemInArray<T = any>(array: T[], fromIndex: number, toIndex: number): void;

// @public
export interface Point {
    // (undocumented)
    x: number;
    // (undocumented)
    y: number;
}

// @public
export type PreviewContainer = 'global' | 'parent' | ElementRef<HTMLElement> | HTMLElement;

// @public
export function transferArrayItem<T = any>(currentArray: T[], targetArray: T[], currentIndex: number, targetIndex: number): void;

// (No @packageDocumentation comment for this package)

```
