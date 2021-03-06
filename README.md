# WMS Glossary

## Overview

![](assets/img/picking-ecosystem.webp)

## 业界标准用词

主要参考对象：Infor WMS，FLUX

bin 库位, strategy key, Transship 转运, Opportunistic 见缝插针, forward pick 预拣货, preset criteria 预先设定标准
appointment 入库预约, task interleaving 任务交叉(叉车去putaway，顺便回来的路上完成一个 picking task)
kitting 配套, assembly 组装, labeling 贴标签,

## Inbound

case level receiving,  single scan receiving, catch weight
putaway restrictions, quality check process, rainbow pallet putaway

## Outbound

### Entities

#### shipment

A `shipment` is a group of sales order or transfer order lines for the same customer or the same delivery address.

#### load

A `load` is a group of sales order or transfer order lines that are grouped together, and that typically go out on a single truck, rail car, or other mode of transport. 

A `load` can have one or many `shipments`. 

You can manually create a load by adding order lines to a new load. 

When orders are released to the warehouse, the system creates `load lines` and groups them into `shipments`.

### Picking 拣货/拣选

- pick method 拣货方式
   - discrete order picking(pick-by-order)
      - one order-picker picks one order, one line at a time
      - ideal for paper based picking
      - 摘果式(Discreet picking)：在一次拣货旅行时中把一个订单中所有需要的商品全部拣出
   - 先拣后播式(Batch picking and Batch sorting)
      - 合并多个订单的需求，在一次行走将一个或多个商品按总量拣出，然后再进行重新分播到各个订单，需要额外的工作场地或设施进行分播处理
   - zone picking 分区接力式
   - batch picking 批量拣货
   - piece picking 零拣
   - cluster picking 集中拣货
      - system-directed cluster picking
   - wave picking
      - wave template
   - zone-batch picking
   - zone-wave picking
   - zone-batch-wave picking

dynamic picking, dynamic case picks, multiple pallet picks, fulfill batch pick orders
pick line grouping

### Outbound sorting


### Loading 装车

RF directed loading, load scheduling, load plan, RF load tasks, shipping loaded orders

### Misc

wave planning, sortation tasks, dynamic allocation & picking,`reallocation, System-directed work sequencing
Organization-wide system directed work sequencing feature

## Item 商品

batch-tracked items 批次管理的商品, material 物料,

## 通用词汇

direct, damage, loss, shortage, scrap rate, lead time, inspection, stock-out rate, label printing, overdue
options, setup, mandatory, partial, the process can be finalized

Single-Piece-Orders (SPO), Multi-Piece-Orders (MPO) 

mass, remedy for

portfolio receipt consolidate

piece picking, case picking, pallet picking, cluster picking, batch picking, 
blind receiving, count back
dock door(Yard Managment System)
operator and supervisor
hard allocation: A WMS process in which the specific location where an item to be picked from is assigned.

预占库存 reserve inventory
sorting(of picked orders): group picked orders by customer orders
Kitting 打包

sales orders, returns, transfer orders, production orders, 

inventory reservation, workload, 

slotting, allocation, pre-allocation, task dispatch strategy, substrategy, order selection and eligibility, order sequencing, lane, pick and drop
cherry pick replenishment tasks, Warehouse slotting, consolidate

due date, tailored, justify,

## References

- [Microsfot Dynamics365 WMS](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)
