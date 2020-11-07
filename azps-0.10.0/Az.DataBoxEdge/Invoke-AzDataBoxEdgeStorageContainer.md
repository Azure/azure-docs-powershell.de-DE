---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: c228b00cb8d0d1e8f238e0b2e75427e0d623490f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844099"
---
# <span data-ttu-id="9a946-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a946-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9a946-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a946-102">SYNOPSIS</span></span>
<span data-ttu-id="9a946-103">Ruft bestimmte Aktionen auf einem Speichercontainer auf</span><span class="sxs-lookup"><span data-stu-id="9a946-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="9a946-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a946-104">SYNTAX</span></span>

### <span data-ttu-id="9a946-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a946-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a946-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a946-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a946-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a946-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a946-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a946-108">DESCRIPTION</span></span>
<span data-ttu-id="9a946-109">Das Cmdlet **Invoke-AzDataBoxEdgeStorageContainer** ruft Aktionen auf, um die Daten auf einem Speichercontainer auf einem Daten Feld-Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9a946-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="9a946-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a946-110">EXAMPLES</span></span>

### <span data-ttu-id="9a946-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a946-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="9a946-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9a946-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="9a946-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a946-113">PARAMETERS</span></span>

### <span data-ttu-id="9a946-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a946-114">-AsJob</span></span>
<span data-ttu-id="9a946-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a946-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a946-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a946-116">-DefaultProfile</span></span>
<span data-ttu-id="9a946-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a946-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a946-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9a946-118">-DeviceName</span></span>
<span data-ttu-id="9a946-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="9a946-119">Device Name</span></span>

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

### <span data-ttu-id="9a946-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9a946-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="9a946-121">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="9a946-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a946-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a946-122">-InputObject</span></span>
<span data-ttu-id="9a946-123">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="9a946-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a946-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9a946-124">-Name</span></span>
<span data-ttu-id="9a946-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="9a946-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a946-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a946-126">-PassThru</span></span>
<span data-ttu-id="9a946-127">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="9a946-127">returns true if successful</span></span>

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

### <span data-ttu-id="9a946-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="9a946-128">-RefreshData</span></span>
<span data-ttu-id="9a946-129">Aktualisieren von Container Metadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="9a946-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="9a946-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a946-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a946-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9a946-131">Resource Group Name</span></span>

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

### <span data-ttu-id="9a946-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a946-132">-ResourceId</span></span>
<span data-ttu-id="9a946-133">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="9a946-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a946-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a946-134">-Confirm</span></span>
<span data-ttu-id="9a946-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a946-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a946-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a946-136">-WhatIf</span></span>
<span data-ttu-id="9a946-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a946-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a946-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a946-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a946-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a946-139">CommonParameters</span></span>
<span data-ttu-id="9a946-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a946-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a946-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a946-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a946-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a946-142">INPUTS</span></span>

### <span data-ttu-id="9a946-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9a946-143">System.String</span></span>

### <span data-ttu-id="9a946-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a946-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9a946-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a946-145">OUTPUTS</span></span>

### <span data-ttu-id="9a946-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a946-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9a946-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a946-147">NOTES</span></span>

## <span data-ttu-id="9a946-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a946-148">RELATED LINKS</span></span>
