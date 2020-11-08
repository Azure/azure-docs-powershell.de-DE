---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004910"
---
# <span data-ttu-id="81d25-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81d25-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="81d25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81d25-102">SYNOPSIS</span></span>
<span data-ttu-id="81d25-103">Erstellt eine Azure Website-Wiederherstellungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="81d25-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="81d25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81d25-104">SYNTAX</span></span>

### <span data-ttu-id="81d25-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="81d25-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d25-106">Azure</span><span class="sxs-lookup"><span data-stu-id="81d25-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d25-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81d25-107">DESCRIPTION</span></span>
<span data-ttu-id="81d25-108">Das Cmdlet **New-AzRecoveryServicesAsrFabric** erstellt ein Azure Site Recovery-Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="81d25-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="81d25-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81d25-109">EXAMPLES</span></span>

### <span data-ttu-id="81d25-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81d25-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="81d25-111">Startet die Fabric-Erstellung mit dem übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Fabric-Erstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81d25-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="81d25-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="81d25-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="81d25-113">Startet die Azure Fabric-Erstellung mit dem übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Fabric-Erstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="81d25-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="81d25-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="81d25-114">PARAMETERS</span></span>

### <span data-ttu-id="81d25-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="81d25-115">-Azure</span></span>
<span data-ttu-id="81d25-116">Der Parameter Switch gibt an, dass Azure Fabric erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81d25-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d25-117">-DefaultProfile</span></span>
<span data-ttu-id="81d25-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81d25-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="81d25-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="81d25-119">-Location</span></span>
<span data-ttu-id="81d25-120">Gibt den Azure-Bereich an, der dem erstellten Fabric-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="81d25-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="81d25-121">Das Azure Site Recovery Fabric-Objekt stellt einen Bereich dar.</span><span class="sxs-lookup"><span data-stu-id="81d25-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="81d25-122">Für virtuelle Computer, die zwischen zwei Azure-Bereichen repliziert werden, stellt ein primärer Stoff den primären Azure-Bereich und den Wiederherstellungs Stoff dar.</span><span class="sxs-lookup"><span data-stu-id="81d25-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d25-123">-Name</span><span class="sxs-lookup"><span data-stu-id="81d25-123">-Name</span></span>
<span data-ttu-id="81d25-124">Gibt den Namen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="81d25-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="81d25-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="81d25-125">-Type</span></span>
<span data-ttu-id="81d25-126">Gibt den Fabric-Typ "Azure Site Recovery" an.</span><span class="sxs-lookup"><span data-stu-id="81d25-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d25-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81d25-127">-Confirm</span></span>
<span data-ttu-id="81d25-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81d25-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d25-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d25-129">-WhatIf</span></span>
<span data-ttu-id="81d25-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81d25-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81d25-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81d25-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d25-132">CommonParameters</span></span>
<span data-ttu-id="81d25-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d25-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d25-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d25-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81d25-135">INPUTS</span></span>

### <span data-ttu-id="81d25-136">Keine</span><span class="sxs-lookup"><span data-stu-id="81d25-136">None</span></span>

## <span data-ttu-id="81d25-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81d25-137">OUTPUTS</span></span>

### <span data-ttu-id="81d25-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="81d25-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81d25-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="81d25-139">NOTES</span></span>

## <span data-ttu-id="81d25-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81d25-140">RELATED LINKS</span></span>

[<span data-ttu-id="81d25-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81d25-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="81d25-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="81d25-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
