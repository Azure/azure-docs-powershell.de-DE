---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174390"
---
# <span data-ttu-id="55fd1-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="55fd1-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="55fd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="55fd1-103">Ruft bestimmte Aktionen für eine Freigabe auf.</span><span class="sxs-lookup"><span data-stu-id="55fd1-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="55fd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55fd1-104">SYNTAX</span></span>

### <span data-ttu-id="55fd1-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55fd1-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55fd1-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55fd1-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55fd1-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55fd1-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55fd1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="55fd1-109">Das Cmdlet **Invoke-AzDataBoxEdgeShare** ruft Aktion auf, um Daten auf einer Freigabe auf einem Daten Feld-Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55fd1-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="55fd1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55fd1-110">EXAMPLES</span></span>

### <span data-ttu-id="55fd1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55fd1-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="55fd1-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55fd1-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="55fd1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="55fd1-113">PARAMETERS</span></span>

### <span data-ttu-id="55fd1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55fd1-114">-AsJob</span></span>
<span data-ttu-id="55fd1-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55fd1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55fd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fd1-116">-DefaultProfile</span></span>
<span data-ttu-id="55fd1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55fd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55fd1-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="55fd1-118">-DeviceName</span></span>
<span data-ttu-id="55fd1-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="55fd1-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55fd1-120">-InputObject</span></span>
<span data-ttu-id="55fd1-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="55fd1-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="55fd1-122">-Name</span></span>
<span data-ttu-id="55fd1-123">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="55fd1-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55fd1-124">-PassThru</span></span>
<span data-ttu-id="55fd1-125">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="55fd1-125">returns true if successful</span></span>

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

### <span data-ttu-id="55fd1-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="55fd1-126">-RefreshData</span></span>
<span data-ttu-id="55fd1-127">Aktualisieren von Freigabe Metadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="55fd1-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="55fd1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fd1-128">-ResourceGroupName</span></span>
<span data-ttu-id="55fd1-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="55fd1-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd1-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55fd1-130">-ResourceId</span></span>
<span data-ttu-id="55fd1-131">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="55fd1-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fd1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55fd1-132">-Confirm</span></span>
<span data-ttu-id="55fd1-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55fd1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55fd1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55fd1-134">-WhatIf</span></span>
<span data-ttu-id="55fd1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55fd1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55fd1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55fd1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55fd1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fd1-137">CommonParameters</span></span>
<span data-ttu-id="55fd1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fd1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fd1-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55fd1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fd1-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55fd1-140">INPUTS</span></span>

### <span data-ttu-id="55fd1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55fd1-141">System.String</span></span>

### <span data-ttu-id="55fd1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="55fd1-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="55fd1-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55fd1-143">OUTPUTS</span></span>

### <span data-ttu-id="55fd1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55fd1-144">System.Boolean</span></span>

## <span data-ttu-id="55fd1-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="55fd1-145">NOTES</span></span>

## <span data-ttu-id="55fd1-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55fd1-146">RELATED LINKS</span></span>
