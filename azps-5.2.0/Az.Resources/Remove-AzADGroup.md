---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296615"
---
# <span data-ttu-id="958b9-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="958b9-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="958b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="958b9-102">SYNOPSIS</span></span>
<span data-ttu-id="958b9-103">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="958b9-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="958b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="958b9-104">SYNTAX</span></span>

### <span data-ttu-id="958b9-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="958b9-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958b9-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="958b9-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958b9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="958b9-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="958b9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="958b9-108">DESCRIPTION</span></span>
<span data-ttu-id="958b9-109">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="958b9-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="958b9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="958b9-110">EXAMPLES</span></span>

### <span data-ttu-id="958b9-111">Beispiel 1: Entfernen einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="958b9-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="958b9-112">Entfernt die Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="958b9-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="958b9-113">Beispiel 2: Entfernen einer Gruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="958b9-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="958b9-114">Ruft die Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' ab und gibt diese an Remove-AzADGroup, um die Gruppe aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="958b9-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="958b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="958b9-115">PARAMETERS</span></span>

### <span data-ttu-id="958b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958b9-116">-DefaultProfile</span></span>
<span data-ttu-id="958b9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="958b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="958b9-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="958b9-118">-DisplayName</span></span>
<span data-ttu-id="958b9-119">Der Anzeigename der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="958b9-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958b9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="958b9-120">-Force</span></span>
<span data-ttu-id="958b9-121">Falls angegeben, wird nicht zur Bestätigung des Löschens der Gruppe gefragt.</span><span class="sxs-lookup"><span data-stu-id="958b9-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="958b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="958b9-122">-InputObject</span></span>
<span data-ttu-id="958b9-123">Die Objektdarstellung der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="958b9-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="958b9-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="958b9-124">-ObjectId</span></span>
<span data-ttu-id="958b9-125">Die Objekt-ID der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="958b9-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958b9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="958b9-126">-PassThru</span></span>
<span data-ttu-id="958b9-127">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="958b9-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="958b9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="958b9-128">-Confirm</span></span>
<span data-ttu-id="958b9-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="958b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958b9-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="958b9-130">-WhatIf</span></span>
<span data-ttu-id="958b9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="958b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958b9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="958b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="958b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958b9-133">CommonParameters</span></span>
<span data-ttu-id="958b9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958b9-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="958b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958b9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="958b9-136">INPUTS</span></span>

### <span data-ttu-id="958b9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="958b9-137">System.String</span></span>

### <span data-ttu-id="958b9-138">Microsoft.Azure.Commands.ActiveDirectory.WERDENDGroup</span><span class="sxs-lookup"><span data-stu-id="958b9-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="958b9-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="958b9-139">OUTPUTS</span></span>

### <span data-ttu-id="958b9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="958b9-140">System.Boolean</span></span>

## <span data-ttu-id="958b9-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="958b9-141">NOTES</span></span>

## <span data-ttu-id="958b9-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="958b9-142">RELATED LINKS</span></span>