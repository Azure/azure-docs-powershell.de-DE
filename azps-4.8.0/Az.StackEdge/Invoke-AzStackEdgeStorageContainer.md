---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: d7e8c65a54adae1de7b7f3ba1ed2d67139638846
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165489"
---
# <span data-ttu-id="6320c-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6320c-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6320c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6320c-102">SYNOPSIS</span></span>
<span data-ttu-id="6320c-103">Ruft bestimmte Aktionen auf einem Speichercontainer auf</span><span class="sxs-lookup"><span data-stu-id="6320c-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="6320c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6320c-104">SYNTAX</span></span>

### <span data-ttu-id="6320c-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6320c-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6320c-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6320c-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6320c-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6320c-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6320c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6320c-108">DESCRIPTION</span></span>
<span data-ttu-id="6320c-109">Das Cmdlet **Invoke-AzStackEdgeStorageContainer** ruft Aktionen auf, um die Daten auf einem Speichercontainer auf einem Stack-Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6320c-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="6320c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6320c-110">EXAMPLES</span></span>

### <span data-ttu-id="6320c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6320c-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="6320c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6320c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="6320c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6320c-113">PARAMETERS</span></span>

### <span data-ttu-id="6320c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6320c-114">-AsJob</span></span>
<span data-ttu-id="6320c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6320c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6320c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6320c-116">-DefaultProfile</span></span>
<span data-ttu-id="6320c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6320c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6320c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6320c-118">-DeviceName</span></span>
<span data-ttu-id="6320c-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="6320c-119">Device Name</span></span>

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

### <span data-ttu-id="6320c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6320c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="6320c-121">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="6320c-121">Resource Name</span></span>

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

### <span data-ttu-id="6320c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6320c-122">-InputObject</span></span>
<span data-ttu-id="6320c-123">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="6320c-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6320c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6320c-124">-Name</span></span>
<span data-ttu-id="6320c-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="6320c-125">Resource Name</span></span>

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

### <span data-ttu-id="6320c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6320c-126">-PassThru</span></span>
<span data-ttu-id="6320c-127">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="6320c-127">returns true if successful</span></span>

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

### <span data-ttu-id="6320c-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="6320c-128">-RefreshData</span></span>
<span data-ttu-id="6320c-129">Aktualisieren von Container Metadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="6320c-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="6320c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6320c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6320c-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6320c-131">Resource Group Name</span></span>

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

### <span data-ttu-id="6320c-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6320c-132">-ResourceId</span></span>
<span data-ttu-id="6320c-133">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="6320c-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="6320c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6320c-134">-Confirm</span></span>
<span data-ttu-id="6320c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6320c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6320c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6320c-136">-WhatIf</span></span>
<span data-ttu-id="6320c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6320c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6320c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6320c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6320c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6320c-139">CommonParameters</span></span>
<span data-ttu-id="6320c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6320c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6320c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6320c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6320c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6320c-142">INPUTS</span></span>

### <span data-ttu-id="6320c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6320c-143">System.String</span></span>

### <span data-ttu-id="6320c-144">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6320c-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6320c-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6320c-145">OUTPUTS</span></span>

### <span data-ttu-id="6320c-146">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6320c-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="6320c-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="6320c-147">NOTES</span></span>

## <span data-ttu-id="6320c-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6320c-148">RELATED LINKS</span></span>
