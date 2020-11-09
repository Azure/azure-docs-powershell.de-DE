---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298683"
---
# <span data-ttu-id="f8708-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8708-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f8708-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8708-102">SYNOPSIS</span></span>
<span data-ttu-id="f8708-103">Entfernt einen Speichercontainer für das Edge-Speicherkonto auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f8708-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="f8708-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8708-104">SYNTAX</span></span>

### <span data-ttu-id="f8708-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8708-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8708-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8708-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8708-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8708-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8708-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8708-108">DESCRIPTION</span></span>
<span data-ttu-id="f8708-109">Mit dem Cmdlet **Remove-AzDataBoxEdgeStorageContainer** wird ein zugeordneter Speichercontainer für das Edge-Speicherkonto auf einem Daten Feld-Edge-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="f8708-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="f8708-110">Sie können den Namen des Speichercontainers angeben, der als Parameter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8708-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="f8708-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8708-111">EXAMPLES</span></span>

### <span data-ttu-id="f8708-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8708-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="f8708-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8708-113">PARAMETERS</span></span>

### <span data-ttu-id="f8708-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8708-114">-AsJob</span></span>
<span data-ttu-id="f8708-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f8708-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8708-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8708-116">-DefaultProfile</span></span>
<span data-ttu-id="f8708-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8708-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8708-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f8708-118">-DeviceName</span></span>
<span data-ttu-id="f8708-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="f8708-119">Device Name</span></span>

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

### <span data-ttu-id="f8708-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8708-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="f8708-121">Angeben des vorhandenen EdgeStorageAccount-namens</span><span class="sxs-lookup"><span data-stu-id="f8708-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="f8708-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8708-122">-InputObject</span></span>
<span data-ttu-id="f8708-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f8708-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8708-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f8708-124">-Name</span></span>
<span data-ttu-id="f8708-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="f8708-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8708-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8708-126">-PassThru</span></span>
<span data-ttu-id="f8708-127">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="f8708-127">returns true if successful</span></span>

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

### <span data-ttu-id="f8708-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8708-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8708-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f8708-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f8708-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8708-130">-ResourceId</span></span>
<span data-ttu-id="f8708-131">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="f8708-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="f8708-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8708-132">-Confirm</span></span>
<span data-ttu-id="f8708-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8708-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8708-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8708-134">-WhatIf</span></span>
<span data-ttu-id="f8708-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8708-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8708-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8708-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8708-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8708-137">CommonParameters</span></span>
<span data-ttu-id="f8708-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8708-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8708-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8708-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8708-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8708-140">INPUTS</span></span>

### <span data-ttu-id="f8708-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f8708-141">System.String</span></span>

### <span data-ttu-id="f8708-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8708-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="f8708-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8708-143">OUTPUTS</span></span>

### <span data-ttu-id="f8708-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8708-144">System.Boolean</span></span>

## <span data-ttu-id="f8708-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8708-145">NOTES</span></span>

## <span data-ttu-id="f8708-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8708-146">RELATED LINKS</span></span>
