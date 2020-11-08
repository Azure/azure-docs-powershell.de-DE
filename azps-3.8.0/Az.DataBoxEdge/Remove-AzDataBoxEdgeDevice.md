---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004780"
---
# <span data-ttu-id="55772-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="55772-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="55772-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55772-102">SYNOPSIS</span></span>
<span data-ttu-id="55772-103">Entfernt ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="55772-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="55772-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55772-104">SYNTAX</span></span>

### <span data-ttu-id="55772-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55772-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55772-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55772-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55772-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55772-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55772-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55772-108">DESCRIPTION</span></span>
<span data-ttu-id="55772-109">Das Cmdlet **Remove-AzDataBoxEdgeDevice** entfernt die Konfiguration für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="55772-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="55772-110">Beachten Sie, dass das Gerät nur gelöscht werden kann, nachdem Sie die Bestellung aufgegeben haben und bevor das Gerät von Microsoft für den versandbereit gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55772-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="55772-111">Lesen Sie die Dokumentation zum Löschen der Ressource, bevor Sie dieses [Cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) verwenden.</span><span class="sxs-lookup"><span data-stu-id="55772-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="55772-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55772-112">EXAMPLES</span></span>

### <span data-ttu-id="55772-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55772-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="55772-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="55772-114">PARAMETERS</span></span>

### <span data-ttu-id="55772-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55772-115">-AsJob</span></span>
<span data-ttu-id="55772-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55772-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55772-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55772-117">-DefaultProfile</span></span>
<span data-ttu-id="55772-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55772-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55772-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55772-119">-InputObject</span></span>
<span data-ttu-id="55772-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="55772-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55772-121">-Name</span><span class="sxs-lookup"><span data-stu-id="55772-121">-Name</span></span>
<span data-ttu-id="55772-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="55772-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55772-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55772-123">-PassThru</span></span>
<span data-ttu-id="55772-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="55772-124">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55772-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55772-125">-ResourceGroupName</span></span>
<span data-ttu-id="55772-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="55772-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55772-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55772-127">-ResourceId</span></span>
<span data-ttu-id="55772-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="55772-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55772-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55772-129">-Confirm</span></span>
<span data-ttu-id="55772-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55772-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55772-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55772-131">-WhatIf</span></span>
<span data-ttu-id="55772-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55772-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55772-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55772-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55772-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55772-134">CommonParameters</span></span>
<span data-ttu-id="55772-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55772-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55772-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55772-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55772-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55772-137">INPUTS</span></span>

### <span data-ttu-id="55772-138">System. String</span><span class="sxs-lookup"><span data-stu-id="55772-138">System.String</span></span>

### <span data-ttu-id="55772-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="55772-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="55772-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55772-140">OUTPUTS</span></span>

### <span data-ttu-id="55772-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55772-141">System.Boolean</span></span>

## <span data-ttu-id="55772-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="55772-142">NOTES</span></span>

## <span data-ttu-id="55772-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55772-143">RELATED LINKS</span></span>
