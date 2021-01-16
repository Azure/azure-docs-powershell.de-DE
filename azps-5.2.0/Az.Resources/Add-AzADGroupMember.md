---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362940"
---
# <span data-ttu-id="446da-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="446da-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="446da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446da-102">SYNOPSIS</span></span>
<span data-ttu-id="446da-103">Fügt einen Benutzer zu einer vorhandenen Ad-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="446da-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="446da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="446da-104">SYNTAX</span></span>

### <span data-ttu-id="446da-105">MemberObjectIdWithGroupObjectId (Standard)</span><span class="sxs-lookup"><span data-stu-id="446da-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446da-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="446da-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446da-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="446da-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446da-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="446da-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446da-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="446da-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="446da-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="446da-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="446da-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="446da-111">DESCRIPTION</span></span>
<span data-ttu-id="446da-112">Fügt einen Benutzer zu einer vorhandenen Ad-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="446da-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="446da-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="446da-113">EXAMPLES</span></span>

### <span data-ttu-id="446da-114">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="446da-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="446da-115">Fügt den Benutzer mit der Objekt-ID 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' zur Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' hinzu.</span><span class="sxs-lookup"><span data-stu-id="446da-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="446da-116">Beispiel 2: Hinzufügen eines Benutzers zu einer Gruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="446da-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="446da-117">Ruft die Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' ab und gibt sie an das cmdlet Add-AzADGroupMember weiter, um den Benutzer dieser Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="446da-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="446da-118">Beispiel 3: Hinzufügen eines Benutzers zu einer Gruppe nach dem Prinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="446da-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="446da-119">Fügt einen Benutzer zu einer Gruppe hinzu und listet die Mitglieder der Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="446da-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="446da-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="446da-120">PARAMETERS</span></span>

### <span data-ttu-id="446da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446da-121">-DefaultProfile</span></span>
<span data-ttu-id="446da-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="446da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="446da-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="446da-123">-MemberObjectId</span></span>
<span data-ttu-id="446da-124">Die Objekt-ID des Members.</span><span class="sxs-lookup"><span data-stu-id="446da-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446da-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="446da-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="446da-126">Der UPN der Mitglieder, die der Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="446da-126">The UPN of the member(s) to add to the group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446da-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="446da-127">-PassThru</span></span>
<span data-ttu-id="446da-128">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="446da-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="446da-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="446da-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="446da-130">Der Anzeigename der Gruppe, der die Mitglieder hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="446da-130">The display name of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446da-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="446da-131">-TargetGroupObject</span></span>
<span data-ttu-id="446da-132">Die Objektdarstellung der Gruppe, der die Member hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="446da-132">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="446da-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="446da-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="446da-134">Die Objekt-ID der Gruppe, der die Member hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="446da-134">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="446da-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="446da-135">-Confirm</span></span>
<span data-ttu-id="446da-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="446da-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="446da-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="446da-137">-WhatIf</span></span>
<span data-ttu-id="446da-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="446da-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446da-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="446da-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="446da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446da-140">CommonParameters</span></span>
<span data-ttu-id="446da-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446da-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="446da-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446da-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="446da-143">INPUTS</span></span>

### <span data-ttu-id="446da-144">Microsoft.Azure.Commands.ActiveDirectory.WERDENDGroup</span><span class="sxs-lookup"><span data-stu-id="446da-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="446da-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="446da-145">OUTPUTS</span></span>

### <span data-ttu-id="446da-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="446da-146">System.Boolean</span></span>

## <span data-ttu-id="446da-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="446da-147">NOTES</span></span>

## <span data-ttu-id="446da-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="446da-148">RELATED LINKS</span></span>
