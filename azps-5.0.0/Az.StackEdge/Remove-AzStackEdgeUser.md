---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175846"
---
# <span data-ttu-id="0cb85-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="0cb85-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="0cb85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cb85-102">SYNOPSIS</span></span>
<span data-ttu-id="0cb85-103">Entfernt einen Benutzer auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="0cb85-103">Removes a user on a device.</span></span>

## <span data-ttu-id="0cb85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cb85-104">SYNTAX</span></span>

### <span data-ttu-id="0cb85-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cb85-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb85-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cb85-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cb85-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cb85-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cb85-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cb85-108">DESCRIPTION</span></span>
<span data-ttu-id="0cb85-109">Das Cmdlet **Remove-AzStackEdgeUser** entfernt einen Benutzer auf dem Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="0cb85-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="0cb85-110">Die Erstellung von nur Benutzertypen `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0cb85-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="0cb85-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cb85-111">EXAMPLES</span></span>

### <span data-ttu-id="0cb85-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0cb85-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="0cb85-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cb85-113">PARAMETERS</span></span>

### <span data-ttu-id="0cb85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cb85-114">-AsJob</span></span>
<span data-ttu-id="0cb85-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0cb85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cb85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cb85-116">-DefaultProfile</span></span>
<span data-ttu-id="0cb85-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cb85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cb85-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0cb85-118">-DeviceName</span></span>
<span data-ttu-id="0cb85-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="0cb85-119">Device Name</span></span>

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

### <span data-ttu-id="0cb85-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0cb85-120">-InputObject</span></span>
<span data-ttu-id="0cb85-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="0cb85-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb85-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0cb85-122">-Name</span></span>
<span data-ttu-id="0cb85-123">Username</span><span class="sxs-lookup"><span data-stu-id="0cb85-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cb85-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cb85-124">-PassThru</span></span>
<span data-ttu-id="0cb85-125">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0cb85-125">returns true if successful</span></span>

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

### <span data-ttu-id="0cb85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cb85-126">-ResourceGroupName</span></span>
<span data-ttu-id="0cb85-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0cb85-127">Resource Group Name</span></span>

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

### <span data-ttu-id="0cb85-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0cb85-128">-ResourceId</span></span>
<span data-ttu-id="0cb85-129">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="0cb85-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="0cb85-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0cb85-130">-Confirm</span></span>
<span data-ttu-id="0cb85-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cb85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cb85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cb85-132">-WhatIf</span></span>
<span data-ttu-id="0cb85-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cb85-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cb85-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cb85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cb85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cb85-135">CommonParameters</span></span>
<span data-ttu-id="0cb85-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cb85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cb85-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cb85-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cb85-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cb85-138">INPUTS</span></span>

### <span data-ttu-id="0cb85-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0cb85-139">System.String</span></span>

### <span data-ttu-id="0cb85-140">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="0cb85-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="0cb85-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cb85-141">OUTPUTS</span></span>

### <span data-ttu-id="0cb85-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="0cb85-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="0cb85-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cb85-143">NOTES</span></span>

## <span data-ttu-id="0cb85-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cb85-144">RELATED LINKS</span></span>
