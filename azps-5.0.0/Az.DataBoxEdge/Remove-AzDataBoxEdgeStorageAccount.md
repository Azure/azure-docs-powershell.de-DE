---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298696"
---
# <span data-ttu-id="ede12-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ede12-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="ede12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ede12-102">SYNOPSIS</span></span>
<span data-ttu-id="ede12-103">Entfernt das Edge-Speicherkonto für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="ede12-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="ede12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ede12-104">SYNTAX</span></span>

### <span data-ttu-id="ede12-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ede12-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ede12-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ede12-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ede12-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ede12-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede12-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ede12-108">DESCRIPTION</span></span>
<span data-ttu-id="ede12-109">Das Cmdlet " **Remove-AzDataBoxEdgeStorageAccount** " entfernt ein zugeordnetes Edge-Speicherkonto für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="ede12-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="ede12-110">Sie können den Namen des Edge-speicherkontos angeben, das als Parameter im Cmdlet entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ede12-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="ede12-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ede12-111">EXAMPLES</span></span>

### <span data-ttu-id="ede12-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ede12-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="ede12-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ede12-113">PARAMETERS</span></span>

### <span data-ttu-id="ede12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ede12-114">-AsJob</span></span>
<span data-ttu-id="ede12-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ede12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ede12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede12-116">-DefaultProfile</span></span>
<span data-ttu-id="ede12-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ede12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede12-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ede12-118">-DeviceName</span></span>
<span data-ttu-id="ede12-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="ede12-119">Device Name</span></span>

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

### <span data-ttu-id="ede12-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ede12-120">-InputObject</span></span>
<span data-ttu-id="ede12-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="ede12-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ede12-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ede12-122">-Name</span></span>
<span data-ttu-id="ede12-123">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="ede12-123">Resource Name</span></span>

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

### <span data-ttu-id="ede12-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ede12-124">-PassThru</span></span>
<span data-ttu-id="ede12-125">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="ede12-125">returns true if successful</span></span>

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

### <span data-ttu-id="ede12-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede12-126">-ResourceGroupName</span></span>
<span data-ttu-id="ede12-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ede12-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ede12-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ede12-128">-ResourceId</span></span>
<span data-ttu-id="ede12-129">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="ede12-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede12-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ede12-130">-Confirm</span></span>
<span data-ttu-id="ede12-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ede12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ede12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede12-132">-WhatIf</span></span>
<span data-ttu-id="ede12-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ede12-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ede12-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ede12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ede12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede12-135">CommonParameters</span></span>
<span data-ttu-id="ede12-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede12-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ede12-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede12-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ede12-138">INPUTS</span></span>

### <span data-ttu-id="ede12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ede12-139">System.String</span></span>

### <span data-ttu-id="ede12-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ede12-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="ede12-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ede12-141">OUTPUTS</span></span>

### <span data-ttu-id="ede12-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ede12-142">System.Boolean</span></span>

## <span data-ttu-id="ede12-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ede12-143">NOTES</span></span>

## <span data-ttu-id="ede12-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ede12-144">RELATED LINKS</span></span>
