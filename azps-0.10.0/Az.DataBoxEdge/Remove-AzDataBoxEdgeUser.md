---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842412"
---
# <span data-ttu-id="dcf9a-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="dcf9a-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="dcf9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dcf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf9a-103">Entfernt einen Benutzer auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-103">Removes a user on a device.</span></span>

## <span data-ttu-id="dcf9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcf9a-104">SYNTAX</span></span>

### <span data-ttu-id="dcf9a-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dcf9a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf9a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf9a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf9a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcf9a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf9a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcf9a-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf9a-109">Das Cmdlet **Remove-AzDataBoxEdgeUser** entfernt einen Benutzer auf dem Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="dcf9a-110">Die Erstellung von nur Benutzertypen `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="dcf9a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcf9a-111">EXAMPLES</span></span>

### <span data-ttu-id="dcf9a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dcf9a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="dcf9a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcf9a-113">PARAMETERS</span></span>

### <span data-ttu-id="dcf9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcf9a-114">-AsJob</span></span>
<span data-ttu-id="dcf9a-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dcf9a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcf9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf9a-116">-DefaultProfile</span></span>
<span data-ttu-id="dcf9a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf9a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dcf9a-118">-DeviceName</span></span>
<span data-ttu-id="dcf9a-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="dcf9a-119">Device Name</span></span>

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

### <span data-ttu-id="dcf9a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dcf9a-120">-InputObject</span></span>
<span data-ttu-id="dcf9a-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="dcf9a-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf9a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dcf9a-122">-Name</span></span>
<span data-ttu-id="dcf9a-123">Username</span><span class="sxs-lookup"><span data-stu-id="dcf9a-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf9a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcf9a-124">-PassThru</span></span>
<span data-ttu-id="dcf9a-125">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="dcf9a-125">returns true if successful</span></span>

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

### <span data-ttu-id="dcf9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="dcf9a-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dcf9a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="dcf9a-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dcf9a-128">-ResourceId</span></span>
<span data-ttu-id="dcf9a-129">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="dcf9a-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="dcf9a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dcf9a-130">-Confirm</span></span>
<span data-ttu-id="dcf9a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf9a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf9a-132">-WhatIf</span></span>
<span data-ttu-id="dcf9a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcf9a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf9a-135">CommonParameters</span></span>
<span data-ttu-id="dcf9a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf9a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcf9a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf9a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dcf9a-138">INPUTS</span></span>

### <span data-ttu-id="dcf9a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf9a-139">System.String</span></span>

### <span data-ttu-id="dcf9a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="dcf9a-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="dcf9a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dcf9a-141">OUTPUTS</span></span>

### <span data-ttu-id="dcf9a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="dcf9a-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="dcf9a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="dcf9a-143">NOTES</span></span>

## <span data-ttu-id="dcf9a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dcf9a-144">RELATED LINKS</span></span>
