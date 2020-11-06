---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501382"
---
# <span data-ttu-id="62722-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62722-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="62722-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62722-102">SYNOPSIS</span></span>
<span data-ttu-id="62722-103">Bearbeitet einen Website Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="62722-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62722-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62722-104">SYNTAX</span></span>

### <span data-ttu-id="62722-105">Appendgroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="62722-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62722-106">Entfernen vongroup</span><span class="sxs-lookup"><span data-stu-id="62722-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62722-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="62722-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62722-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="62722-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62722-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="62722-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62722-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="62722-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62722-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62722-111">DESCRIPTION</span></span>
<span data-ttu-id="62722-112">Das Cmdlet " **Edit-AzureRmSiteRecoveryRecoveryPlan** " bearbeitet einen Azure Site Recovery-Plan.</span><span class="sxs-lookup"><span data-stu-id="62722-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="62722-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62722-113">EXAMPLES</span></span>

## <span data-ttu-id="62722-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="62722-114">PARAMETERS</span></span>

### <span data-ttu-id="62722-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="62722-115">-AddProtectedEntities</span></span>
<span data-ttu-id="62722-116">Gibt ein Array von geschützten Entitäten an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="62722-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="62722-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-118">-Appendgroup</span><span class="sxs-lookup"><span data-stu-id="62722-118">-AppendGroup</span></span>
<span data-ttu-id="62722-119">Gibt an, dass diese Operation die Gruppe an das Wiederherstellungsplan-Objekt anfügt.</span><span class="sxs-lookup"><span data-stu-id="62722-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62722-120">-DefaultProfile</span></span>
<span data-ttu-id="62722-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62722-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-122">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="62722-122">-Group</span></span>
<span data-ttu-id="62722-123">Gibt eine Gruppe für den Website Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="62722-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62722-124">-RecoveryPlan</span></span>
<span data-ttu-id="62722-125">Gibt einen Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="62722-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62722-126">-Removegroup</span><span class="sxs-lookup"><span data-stu-id="62722-126">-RemoveGroup</span></span>
<span data-ttu-id="62722-127">Entfernt die angegebene Gruppe für den angegebenen Wiederherstellungsplan für eine Website.</span><span class="sxs-lookup"><span data-stu-id="62722-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="62722-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="62722-129">Gibt ein Array von geschützten Entitäten an.</span><span class="sxs-lookup"><span data-stu-id="62722-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="62722-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62722-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62722-131">CommonParameters</span></span>
<span data-ttu-id="62722-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62722-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62722-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62722-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62722-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62722-134">INPUTS</span></span>

### <span data-ttu-id="62722-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62722-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="62722-136">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="62722-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="62722-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62722-137">OUTPUTS</span></span>

## <span data-ttu-id="62722-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="62722-138">NOTES</span></span>

## <span data-ttu-id="62722-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62722-139">RELATED LINKS</span></span>

[<span data-ttu-id="62722-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62722-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="62722-141">Neu – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62722-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
