#### 1.原流程
1. 根据方块数据生成mesh
    CustomModel::load
    CustomModel::genGeomTemplate()
    CustomModel::genGeomTemplateInternal
    BlockMaterialMgr::genGeomTemplate

2. Rainbow::Mesh序列化
   参考这里  
   ![](./Source/Image/2024-10-30-17-52-03.png)  
   ![](./Source/Image/2024-10-30-17-52-39.png)  

    if (obj->IsKindOf<Asset>())
    {
        Asset* asset = static_cast<Asset*>(obj);
        asset->SetResPath(fullPath.c_str());
        GetMetaLoader().CreateAssetAndMeta(guid, asset);
    }
