---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459716"
---
# <span data-ttu-id="799f9-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="799f9-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="799f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799f9-102">SYNOPSIS</span></span>
<span data-ttu-id="799f9-103">Erstellt eine ASR-Netzwerkzuordnung zwischen zwei Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="799f9-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="799f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="799f9-104">SYNTAX</span></span>

### <span data-ttu-id="799f9-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="799f9-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="799f9-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="799f9-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="799f9-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="799f9-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="799f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="799f9-108">DESCRIPTION</span></span>
<span data-ttu-id="799f9-109">Das Cmdlet **"New-AzRecoveryServicesAsrNetworkMapping"** startet den Vorgang zum Erstellen einer ASR-Netzwerkzuordnung zwischen zwei Netzwerken und gibt das Objekt des ASR-Auftrags für den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="799f9-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="799f9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="799f9-110">EXAMPLES</span></span>

### <span data-ttu-id="799f9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="799f9-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="799f9-112">Startet den Vorgang zum Erstellen von Netzwerkzuordnungen unter Verwendung des angegebenen Namens, der primären Netzwerke und der Wiederherstellungsnetzwerke und gibt einen ASR-Auftrag zum Nachverfolgen des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="799f9-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="799f9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="799f9-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="799f9-114">Startet die Netzwerkzuordnung für den Erstellungsvorgang unter Verwendung des angegebenen Namens, der primären Netzwerke und der Wiederherstellungsnetzwerke und gibt einen ASR-Auftrag zurück, um den Vorgang nachverfolgt (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="799f9-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="799f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="799f9-115">PARAMETERS</span></span>

### <span data-ttu-id="799f9-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="799f9-116">-AzureToAzure</span></span>
<span data-ttu-id="799f9-117">Zum Erstellen eines AzureToAzure-Szenarios kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="799f9-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799f9-118">-DefaultProfile</span></span>
<span data-ttu-id="799f9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="799f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="799f9-120">-Name</span></span>
<span data-ttu-id="799f9-121">Name der zu erstellende ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="799f9-121">Name of the ASR network mapping to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="799f9-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="799f9-123">Gibt die virtuelle Azure-Netzwerk-ID des primären Netzwerks für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="799f9-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="799f9-124">-PrimaryFabric</span></span>
<span data-ttu-id="799f9-125">Specifies the ASR fabric where mapping should be created.</span><span class="sxs-lookup"><span data-stu-id="799f9-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="799f9-126">-PrimaryNetwork</span></span>
<span data-ttu-id="799f9-127">Gibt das primäre Netzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="799f9-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="799f9-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="799f9-129">Gibt die Azure-Netzwerk-ID der Wiederherstellung für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="799f9-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="799f9-130">-RecoveryFabric</span></span>
<span data-ttu-id="799f9-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span><span class="sxs-lookup"><span data-stu-id="799f9-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="799f9-132">-RecoveryNetwork</span></span>
<span data-ttu-id="799f9-133">Gibt das Wiederherstellungsnetzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="799f9-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="799f9-134">-Confirm</span></span>
<span data-ttu-id="799f9-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="799f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="799f9-136">-WhatIf</span></span>
<span data-ttu-id="799f9-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="799f9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="799f9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="799f9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="799f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799f9-139">CommonParameters</span></span>
<span data-ttu-id="799f9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="799f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799f9-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="799f9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799f9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="799f9-142">INPUTS</span></span>

### <span data-ttu-id="799f9-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="799f9-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="799f9-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="799f9-144">OUTPUTS</span></span>

### <span data-ttu-id="799f9-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="799f9-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="799f9-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="799f9-146">NOTES</span></span>

## <span data-ttu-id="799f9-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="799f9-147">RELATED LINKS</span></span>

[<span data-ttu-id="799f9-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="799f9-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="799f9-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="799f9-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
