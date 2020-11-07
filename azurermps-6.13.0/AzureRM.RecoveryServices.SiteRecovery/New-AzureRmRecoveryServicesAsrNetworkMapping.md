---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e9aadbc8eae9703340043dc640f4cb9759b919d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662164"
---
# <span data-ttu-id="0fabf-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0fabf-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0fabf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fabf-102">SYNOPSIS</span></span>
<span data-ttu-id="0fabf-103">Erstellt eine ASR-Netzwerkzuordnung zwischen zwei Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="0fabf-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fabf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fabf-104">SYNTAX</span></span>

### <span data-ttu-id="0fabf-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fabf-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fabf-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0fabf-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fabf-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="0fabf-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fabf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fabf-108">DESCRIPTION</span></span>
<span data-ttu-id="0fabf-109">Das Cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** startet den Vorgang des Erstellens einer ASR-Netzwerkzuordnung zwischen zwei Netzwerken und gibt das ASR-Auftragsobjekt für den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fabf-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0fabf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fabf-110">EXAMPLES</span></span>

### <span data-ttu-id="0fabf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fabf-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="0fabf-112">Startet den Netzwerk Zuordnungs Erstellungsvorgang mit dem angegebenen Namen, Primär-und Wiederherstellungs Netz und gibt einen ASR-Auftrag zurück, um den Vorgang zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="0fabf-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="0fabf-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0fabf-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="0fabf-114">Startet die Netzwerkzuordnung für den Erstellungsvorgang mit dem angegebenen Namen, dem primären und dem Wiederherstellungs Netzwerk und gibt einen ASR-Auftrag zurück, um den Vorgang zu überwachen (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="0fabf-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="0fabf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fabf-115">PARAMETERS</span></span>

### <span data-ttu-id="0fabf-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="0fabf-116">-AzureToAzure</span></span>
<span data-ttu-id="0fabf-117">Parameter Switch gibt an, dass die erstellte Netzwerkzuordnung verwendet wird, um Azure Virtual Machines zwischen zwei Azure-Regionen zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="0fabf-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="0fabf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fabf-118">-DefaultProfile</span></span>
<span data-ttu-id="0fabf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fabf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fabf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0fabf-120">-Name</span></span>
<span data-ttu-id="0fabf-121">Der Name der zu erstellende ASR-Netzwerkzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0fabf-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="0fabf-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="0fabf-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="0fabf-123">Gibt die Azure Virtual Network-ID des primären Netzwerks für die Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0fabf-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="0fabf-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="0fabf-124">-PrimaryFabric</span></span>
<span data-ttu-id="0fabf-125">Gibt an Sie den ASR-Stoff, in dem die Zuordnung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fabf-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="0fabf-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="0fabf-126">-PrimaryNetwork</span></span>
<span data-ttu-id="0fabf-127">Gibt das primäre Netzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0fabf-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="0fabf-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="0fabf-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="0fabf-129">Gibt die Azure-Wiederherstellungs-ID für die Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0fabf-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="0fabf-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="0fabf-130">-RecoveryFabric</span></span>
<span data-ttu-id="0fabf-131">Das Azure Site Recovery Fabric-Objekt, das dem Wiederherstellungs-Azure-Bereich entspricht.</span><span class="sxs-lookup"><span data-stu-id="0fabf-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="0fabf-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="0fabf-132">-RecoveryNetwork</span></span>
<span data-ttu-id="0fabf-133">Gibt das Wiederherstellungs Netzwerkobjekt für die ASR-Netzwerkzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0fabf-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="0fabf-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fabf-134">-Confirm</span></span>
<span data-ttu-id="0fabf-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fabf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fabf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fabf-136">-WhatIf</span></span>
<span data-ttu-id="0fabf-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fabf-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fabf-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fabf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fabf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fabf-139">CommonParameters</span></span>
<span data-ttu-id="0fabf-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fabf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fabf-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fabf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fabf-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fabf-142">INPUTS</span></span>

### <span data-ttu-id="0fabf-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="0fabf-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="0fabf-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fabf-144">OUTPUTS</span></span>

### <span data-ttu-id="0fabf-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0fabf-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0fabf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fabf-146">NOTES</span></span>

## <span data-ttu-id="0fabf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fabf-147">RELATED LINKS</span></span>

[<span data-ttu-id="0fabf-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0fabf-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0fabf-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0fabf-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
