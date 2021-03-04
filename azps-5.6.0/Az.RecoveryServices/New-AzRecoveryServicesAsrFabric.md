---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944764"
---
# <span data-ttu-id="65b27-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="65b27-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="65b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b27-102">SYNOPSIS</span></span>
<span data-ttu-id="65b27-103">Erstellt ein Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="65b27-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="65b27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65b27-104">SYNTAX</span></span>

### <span data-ttu-id="65b27-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="65b27-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b27-106">Azure</span><span class="sxs-lookup"><span data-stu-id="65b27-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b27-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65b27-107">DESCRIPTION</span></span>
<span data-ttu-id="65b27-108">Das **Cmdlet New-AzRecoveryServicesAsrFabric** erstellt eine Azure-Websitewiederherstellungs-Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="65b27-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="65b27-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65b27-109">EXAMPLES</span></span>

### <span data-ttu-id="65b27-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65b27-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="65b27-111">Startet die Fabricerstellung mit übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Fabricerstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65b27-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="65b27-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="65b27-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="65b27-113">Startet die Erstellung von Azure Fabric mit übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Fabricerstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65b27-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="65b27-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="65b27-114">PARAMETERS</span></span>

### <span data-ttu-id="65b27-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="65b27-115">-Azure</span></span>
<span data-ttu-id="65b27-116">Parameter "Switch" gibt an, um Azure Fabric zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="65b27-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="65b27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b27-117">-DefaultProfile</span></span>
<span data-ttu-id="65b27-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65b27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="65b27-119">-Location</span><span class="sxs-lookup"><span data-stu-id="65b27-119">-Location</span></span>
<span data-ttu-id="65b27-120">Gibt die Azure-Region an, die dem zu erstellenden Fabric-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="65b27-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="65b27-121">Das Azure Site Recovery-Fabricobjekt stellt eine Region dar.</span><span class="sxs-lookup"><span data-stu-id="65b27-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="65b27-122">Bei virtuellen Computern, die zwischen zwei Azure-Regionen repliziert werden, stellt ein primärer Fabric die primäre Azure-Region und die Wiederherstellungsstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="65b27-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="65b27-123">-Name</span><span class="sxs-lookup"><span data-stu-id="65b27-123">-Name</span></span>
<span data-ttu-id="65b27-124">Gibt den Namen des Azure Site Recovery Fabric an.</span><span class="sxs-lookup"><span data-stu-id="65b27-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="65b27-125">-Type</span><span class="sxs-lookup"><span data-stu-id="65b27-125">-Type</span></span>
<span data-ttu-id="65b27-126">Gibt den Fabrictyp der Azure-Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="65b27-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="65b27-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65b27-127">-Confirm</span></span>
<span data-ttu-id="65b27-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65b27-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b27-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b27-129">-WhatIf</span></span>
<span data-ttu-id="65b27-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65b27-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65b27-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65b27-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b27-132">CommonParameters</span></span>
<span data-ttu-id="65b27-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b27-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b27-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65b27-135">INPUTS</span></span>

### <span data-ttu-id="65b27-136">Keine</span><span class="sxs-lookup"><span data-stu-id="65b27-136">None</span></span>

## <span data-ttu-id="65b27-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65b27-137">OUTPUTS</span></span>

### <span data-ttu-id="65b27-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="65b27-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="65b27-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="65b27-139">NOTES</span></span>

## <span data-ttu-id="65b27-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="65b27-140">RELATED LINKS</span></span>

[<span data-ttu-id="65b27-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="65b27-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="65b27-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="65b27-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
