---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502373"
---
# <span data-ttu-id="2f552-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2f552-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="2f552-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f552-102">SYNOPSIS</span></span>
<span data-ttu-id="2f552-103">Erstellt einen Website Wiederherstellungsplan in der Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="2f552-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f552-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f552-104">SYNTAX</span></span>

### <span data-ttu-id="2f552-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f552-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f552-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="2f552-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f552-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="2f552-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f552-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="2f552-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f552-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="2f552-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f552-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="2f552-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f552-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f552-111">DESCRIPTION</span></span>
<span data-ttu-id="2f552-112">Das Cmdlet **New-AzureRmSiteRecoveryRecoveryPlan** erstellt einen Wiederherstellungsplan in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2f552-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="2f552-113">Ein Wiederherstellungsplan sammelt virtuelle Computer in einer Gruppe, um Failover und Wiederherstellung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f552-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="2f552-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f552-114">EXAMPLES</span></span>

### <span data-ttu-id="2f552-115">Beispiel 1: Hinzufügen eines Wiederherstellungsplans zu einem Website Wiederherstellungs Tresor</span><span class="sxs-lookup"><span data-stu-id="2f552-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="2f552-116">Mit diesem Befehl wird der Wiederherstellungsplan mit dem Namen RecoveryPlan.xml zum Azure Site Recovery Vault hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2f552-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2f552-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f552-117">PARAMETERS</span></span>

### <span data-ttu-id="2f552-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="2f552-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f552-119">-DefaultProfile</span></span>
<span data-ttu-id="2f552-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f552-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f552-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="2f552-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2f552-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-123">-Path</span><span class="sxs-lookup"><span data-stu-id="2f552-123">-Path</span></span>
<span data-ttu-id="2f552-124">Gibt den Pfad der Wiederherstellungsplan Datei an.</span><span class="sxs-lookup"><span data-stu-id="2f552-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="2f552-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="2f552-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="2f552-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="2f552-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2f552-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="2f552-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2f552-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f552-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f552-132">CommonParameters</span></span>
<span data-ttu-id="2f552-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f552-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f552-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f552-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f552-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f552-135">INPUTS</span></span>

### <span data-ttu-id="2f552-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="2f552-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="2f552-137">Der Parameter "ProtectionEntityList" akzeptiert den Wert vom Typ "ASRProtectionEntity []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2f552-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="2f552-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="2f552-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="2f552-139">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2f552-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="2f552-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f552-140">OUTPUTS</span></span>

## <span data-ttu-id="2f552-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f552-141">NOTES</span></span>

## <span data-ttu-id="2f552-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f552-142">RELATED LINKS</span></span>

[<span data-ttu-id="2f552-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2f552-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2f552-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2f552-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2f552-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2f552-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


