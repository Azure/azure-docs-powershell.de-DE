---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176834"
---
# <span data-ttu-id="e4f69-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e4f69-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e4f69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4f69-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f69-103">Entfernt einen Speichercontainer für das Edge-Speicherkonto auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="e4f69-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="e4f69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4f69-104">SYNTAX</span></span>

### <span data-ttu-id="e4f69-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4f69-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f69-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f69-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f69-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f69-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f69-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4f69-108">DESCRIPTION</span></span>
<span data-ttu-id="e4f69-109">Mit dem Cmdlet **Remove-AzStackEdgeStorageContainer** wird ein zugeordneter Speichercontainer für das edgespeicher-Konto auf einem Stack-Edge-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="e4f69-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="e4f69-110">Sie können den Namen des Speichercontainers angeben, der als Parameter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4f69-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="e4f69-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4f69-111">EXAMPLES</span></span>

### <span data-ttu-id="e4f69-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e4f69-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="e4f69-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4f69-113">PARAMETERS</span></span>

### <span data-ttu-id="e4f69-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4f69-114">-AsJob</span></span>
<span data-ttu-id="e4f69-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e4f69-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4f69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f69-116">-DefaultProfile</span></span>
<span data-ttu-id="e4f69-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e4f69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f69-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e4f69-118">-DeviceName</span></span>
<span data-ttu-id="e4f69-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="e4f69-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f69-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e4f69-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="e4f69-121">Angeben des vorhandenen EdgeStorageAccount-namens</span><span class="sxs-lookup"><span data-stu-id="e4f69-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f69-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e4f69-122">-InputObject</span></span>
<span data-ttu-id="e4f69-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e4f69-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f69-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e4f69-124">-Name</span></span>
<span data-ttu-id="e4f69-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="e4f69-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f69-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4f69-126">-PassThru</span></span>
<span data-ttu-id="e4f69-127">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="e4f69-127">returns true if successful</span></span>

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

### <span data-ttu-id="e4f69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f69-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4f69-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e4f69-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f69-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e4f69-130">-ResourceId</span></span>
<span data-ttu-id="e4f69-131">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="e4f69-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="e4f69-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e4f69-132">-Confirm</span></span>
<span data-ttu-id="e4f69-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e4f69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f69-134">-WhatIf</span></span>
<span data-ttu-id="e4f69-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e4f69-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4f69-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4f69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f69-137">CommonParameters</span></span>
<span data-ttu-id="e4f69-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f69-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4f69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f69-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4f69-140">INPUTS</span></span>

### <span data-ttu-id="e4f69-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f69-141">System.String</span></span>

### <span data-ttu-id="e4f69-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e4f69-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e4f69-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4f69-143">OUTPUTS</span></span>

### <span data-ttu-id="e4f69-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4f69-144">System.Boolean</span></span>

## <span data-ttu-id="e4f69-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4f69-145">NOTES</span></span>

## <span data-ttu-id="e4f69-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4f69-146">RELATED LINKS</span></span>
