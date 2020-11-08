---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177063"
---
# <span data-ttu-id="d5c9f-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5c9f-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d5c9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c9f-103">Erstellt eine Azure Website-Wiederherstellungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="d5c9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5c9f-104">SYNTAX</span></span>

### <span data-ttu-id="d5c9f-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5c9f-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c9f-106">Azure</span><span class="sxs-lookup"><span data-stu-id="d5c9f-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c9f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5c9f-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c9f-108">Das Cmdlet **New-AzRecoveryServicesAsrFabric** erstellt ein Azure Site Recovery-Fabric des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="d5c9f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5c9f-109">EXAMPLES</span></span>

### <span data-ttu-id="d5c9f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5c9f-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="d5c9f-111">Startet die Fabric-Erstellung mit dem übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Fabric-Erstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="d5c9f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5c9f-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="d5c9f-113">Startet die Azure Fabric-Erstellung mit dem übergebenen Namen und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Fabric-Erstellungsvorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="d5c9f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5c9f-114">PARAMETERS</span></span>

### <span data-ttu-id="d5c9f-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="d5c9f-115">-Azure</span></span>
<span data-ttu-id="d5c9f-116">Der Parameter Switch gibt an, dass Azure Fabric erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="d5c9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c9f-117">-DefaultProfile</span></span>
<span data-ttu-id="d5c9f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d5c9f-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="d5c9f-119">-Location</span></span>
<span data-ttu-id="d5c9f-120">Gibt den Azure-Bereich an, der dem erstellten Fabric-Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="d5c9f-121">Das Azure Site Recovery Fabric-Objekt stellt einen Bereich dar.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="d5c9f-122">Für virtuelle Computer, die zwischen zwei Azure-Bereichen repliziert werden, stellt ein primärer Stoff den primären Azure-Bereich und den Wiederherstellungs Stoff dar.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="d5c9f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d5c9f-123">-Name</span></span>
<span data-ttu-id="d5c9f-124">Gibt den Namen des Azure Site Recovery-Fabrics an.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="d5c9f-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="d5c9f-125">-Type</span></span>
<span data-ttu-id="d5c9f-126">Gibt den Fabric-Typ "Azure Site Recovery" an.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="d5c9f-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5c9f-127">-Confirm</span></span>
<span data-ttu-id="d5c9f-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c9f-129">-WhatIf</span></span>
<span data-ttu-id="d5c9f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5c9f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c9f-132">CommonParameters</span></span>
<span data-ttu-id="d5c9f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c9f-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5c9f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c9f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5c9f-135">INPUTS</span></span>

### <span data-ttu-id="d5c9f-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d5c9f-136">None</span></span>

## <span data-ttu-id="d5c9f-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5c9f-137">OUTPUTS</span></span>

### <span data-ttu-id="d5c9f-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5c9f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5c9f-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5c9f-139">NOTES</span></span>

## <span data-ttu-id="d5c9f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5c9f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5c9f-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5c9f-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d5c9f-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d5c9f-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
