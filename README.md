# -
雅典娜之心
▼+N
    [fields]
   +AddNewlyMinedBlock : newBlockFunc
   +BlockSub : ps.Subscription
   +Blockstore : bstore.Blockstore
   +Bootstrapper : *filnet.Bootstrapper
   +ChainReader : chain.ReadStore
   +Consensus : consensus.Protocol
   +Exchange : exchange.Interface
   +HeaviestTipSetCh : chan interface{}
   +HeaviestTipSetHandled : func()
   +HelloSvc : *hello.Handler
   +MessageSub : ps.Subscription
   +MiningScheduler : mining.Scheduler
   +MsgPool : *core.MessagePool
   +OfflineMode : bool
   +OnlineStore : *hamt.CborIpldStore
   +PeerHost : host.Host
   +Ping : *ping.PingService
   +PorcelainAPI : *porcelain.API
   +PowerTable : consensus.PowerTableView
   +Repo : repo.Repo
   +RetrievalClient : *retrieval.Client
   +RetrievalMiner : *retrieval.Miner
   +Router : routing.IpfsRouting
   +StorageMiner : *storage.Miner
   +StorageMinerClient : *storage.Client
   +Syncer : chain.Syncer
   +Wallet : *wallet.Wallet
   -blockTime : time.Duration
   -blockservice : bserv.BlockService
   -cancelMining : context.CancelFunc
   -cancelSubscriptionsCtx : context.CancelFunc
   -cborStore : *hamt.CborIpldStore
   -host : host.Host
   -lookup : lookup.PeerLookupService
   -miningCtx : context.Context
   -miningDoneWg : *sync.WaitGroup
   -sectorBuilder : sectorbuilder.SectorBuilder
    [methods]
   +BlockHeight() : *types.BlockHeight, erro
   +BlockService() : bserv.BlockService
   +CborStore() : *hamt.CborIpldStore
   +ChainReadStore() : chain.ReadStore
   +CreateMiner(ctx context.Context, accountAddr address.Address, gasPrice types.AttoFIL, gasLimit types.GasUnits, pledge uint64, pid libp2ppeer.ID, collateral *types.AttoFIL) : *address.Address, error
   +GetBlockTime() : time.Duration
   +Host() : host.Host
   +Lookup() : lookup.PeerLookupService
   +MiningSignerAddress() : address.Address
   +MiningTimes() : time.Duration, time.Duration
   +SectorBuilder() : sectorbuilder.SectorBuilder
   +SetBlockTime(blockTime time.Duration)
  art(ctx context.Context) : erro
   +Stop(ctx context.Context)
   +StopMining(ctx context.Context)
   -addNewlyMinedBlock(ctx context.Context, b *types.Block)
   -cancelSubscriptions()
   -getMinerActorPubKey() : []byte, error
   -handleNewHeaviestTipSet(ctx context.Context, head types.TipSet)
   -handleNewMiningOutput(miningOutCh chan mining.Output)
   -handleSubscription(ctx context.Context, f pubSubProcessorFunc, fname string, s ps.Subscription, sname string)
   -isMining() : bool
   -miningOwnerAddress(ctx context.Context, miningAddr address.Address) : address.Address, error
   -setIsMining(isMining bool)
    [functions]
   +New(ctx context.Context, opts ...ConfigOpt) : *Node, error
