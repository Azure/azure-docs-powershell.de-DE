---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300262"
---
# <span data-ttu-id="c7a69-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7a69-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c7a69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7a69-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a69-103">Erstellt eine ASR-Netzwerkzuordnung zwischen zwei Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="c7a69-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="c7a69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7a69-104">SYNTAX</span></span>

### <span data-ttu-id="c7a69-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7a69-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7a69-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c7a69-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a69-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c7a69-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a69-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7a69-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a69-109">Das Cmdlet **New-AzRecoveryServicesAsrNetworkMapping** startet den Vorgang des Erstellens einer ASR-Netzwerkzuordnung zwischen zwei Netzwerken und gibt das ASR-Auftragsobjekt für den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7a69-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c7a69-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7a69-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a69-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7a69-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="c7a69-112">Startet den Netzwerk Zuordnungs Erstellungsvorgang mit dem angegebenen Namen, Primär-und Wiederherstellungs Netz und gibt einen ASR-Auftrag zurück, um den Vorgang zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c7a69-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="c7a69-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c7a69-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="c7a69-114">Startet die Netzwerkzuordnung für den Erstellungsvorgang mit dem angegebenen Namen, dem primären und dem Wiederherstellungs Netzwerk und gibt einen ASR-Auftrag zurück, um den Vorgang zu überwachen (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="c7a69-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="c7a69-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7a69-115">PARAMETERS</span></span>

### <span data-ttu-id="c7a69-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c7a69-116">-AzureToAzure</span></span>
<span data-ttu-id="c7a69-117">Flag zum Erstellen eines AzureToAzure-Szenarios</span><span class="sxs-lookup"><span data-stu-id="c7a69-117">Flag to create AzureToAzure scenario.</span></span>

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

### <span data-ttu-id="c7a69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a69-118">-DefaultProfile</span></span>
<span data-ttu-id="c7a69-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7a69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c7a69-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c7a69-120">-Name</span></span>
<span data-ttu-id="c7a69-121">Der Name der zu erstellende ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="c7a69-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="c7a69-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7a69-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="c7a69-123">Gibt die Azure Virtual Network-ID des primären Netzwerks für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c7a69-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="c7a69-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="c7a69-124">-PrimaryFabric</span></span>
<span data-ttu-id="c7a69-125">Gibt den ASR-Stoff an, in dem die Zuordnung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7a69-125">Specifies the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="c7a69-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7a69-126">-PrimaryNetwork</span></span>
<span data-ttu-id="c7a69-127">Gibt das primäre Netzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c7a69-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="c7a69-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c7a69-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="c7a69-129">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c7a69-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="c7a69-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="c7a69-130">-RecoveryFabric</span></span>
<span data-ttu-id="c7a69-131">Das Azure Site Recovery Fabric-Objekt, das dem Wiederherstellungs-Azure-Bereich entspricht.</span><span class="sxs-lookup"><span data-stu-id="c7a69-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="c7a69-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c7a69-132">-RecoveryNetwork</span></span>
<span data-ttu-id="c7a69-133">Gibt das Wiederherstellungs Netzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="c7a69-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="c7a69-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7a69-134">-Confirm</span></span>
<span data-ttu-id="c7a69-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7a69-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a69-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a69-136">-WhatIf</span></span>
<span data-ttu-id="c7a69-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7a69-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7a69-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7a69-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a69-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a69-139">CommonParameters</span></span>
<span data-ttu-id="c7a69-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a69-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a69-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7a69-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a69-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7a69-142">INPUTS</span></span>

### <span data-ttu-id="c7a69-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c7a69-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c7a69-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7a69-144">OUTPUTS</span></span>

### <span data-ttu-id="c7a69-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c7a69-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c7a69-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7a69-146">NOTES</span></span>

## <span data-ttu-id="c7a69-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7a69-147">RELATED LINKS</span></span>

[<span data-ttu-id="c7a69-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7a69-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c7a69-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c7a69-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
