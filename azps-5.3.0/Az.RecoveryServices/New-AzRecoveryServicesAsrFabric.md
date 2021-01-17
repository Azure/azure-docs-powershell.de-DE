---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471618"
---
# <span data-ttu-id="3e8a0-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3e8a0-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3e8a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8a0-103">Creates an Azure Site Recovery Fabric.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="3e8a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e8a0-104">SYNTAX</span></span>

### <span data-ttu-id="3e8a0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e8a0-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e8a0-106">Azure</span><span class="sxs-lookup"><span data-stu-id="3e8a0-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e8a0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e8a0-107">DESCRIPTION</span></span>
<span data-ttu-id="3e8a0-108">Das **Cmdlet "New-AzRecoveryServicesAsrFabric"** erstellt eine Azure Site Recovery Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="3e8a0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="3e8a0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e8a0-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="3e8a0-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="3e8a0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3e8a0-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="3e8a0-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="3e8a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-114">PARAMETERS</span></span>

### <span data-ttu-id="3e8a0-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="3e8a0-115">-Azure</span></span>
<span data-ttu-id="3e8a0-116">Switch parameter specifies to create azure fabric.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="3e8a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8a0-117">-DefaultProfile</span></span>
<span data-ttu-id="3e8a0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3e8a0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3e8a0-119">-Location</span></span>
<span data-ttu-id="3e8a0-120">Gibt die Azure-Region an, die dem erstellten Fabric-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="3e8a0-121">Das Azure Site Recovery Fabric-Objekt stellt eine Region dar.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="3e8a0-122">Bei virtuellen Computern, die zwischen zwei Azure-Regionen repliziert werden, stellt ein primäres Fabric die primäre Azure-Region und die Wiederherstellungsstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="3e8a0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3e8a0-123">-Name</span></span>
<span data-ttu-id="3e8a0-124">Gibt den Namen des Azure Site Recovery Fabric an.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="3e8a0-125">-Type</span><span class="sxs-lookup"><span data-stu-id="3e8a0-125">-Type</span></span>
<span data-ttu-id="3e8a0-126">Gibt den Azure Site Recovery Fabric Type an.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="3e8a0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e8a0-127">-Confirm</span></span>
<span data-ttu-id="3e8a0-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e8a0-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3e8a0-129">-WhatIf</span></span>
<span data-ttu-id="3e8a0-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e8a0-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e8a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8a0-132">CommonParameters</span></span>
<span data-ttu-id="3e8a0-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8a0-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e8a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8a0-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e8a0-135">INPUTS</span></span>

### <span data-ttu-id="3e8a0-136">Keine</span><span class="sxs-lookup"><span data-stu-id="3e8a0-136">None</span></span>

## <span data-ttu-id="3e8a0-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e8a0-137">OUTPUTS</span></span>

### <span data-ttu-id="3e8a0-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3e8a0-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3e8a0-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3e8a0-139">NOTES</span></span>

## <span data-ttu-id="3e8a0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3e8a0-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e8a0-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3e8a0-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3e8a0-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3e8a0-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
