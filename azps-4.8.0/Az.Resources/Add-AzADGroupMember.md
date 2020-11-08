---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008269"
---
# <span data-ttu-id="67e61-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="67e61-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="67e61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67e61-102">SYNOPSIS</span></span>
<span data-ttu-id="67e61-103">Fügt einen Benutzer zu einer vorhandenen Anzeigengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="67e61-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="67e61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67e61-104">SYNTAX</span></span>

### <span data-ttu-id="67e61-105">MemberObjectIdWithGroupObjectId (Standard)</span><span class="sxs-lookup"><span data-stu-id="67e61-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e61-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="67e61-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e61-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="67e61-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e61-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e61-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e61-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e61-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e61-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67e61-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e61-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67e61-111">DESCRIPTION</span></span>
<span data-ttu-id="67e61-112">Fügt einen Benutzer zu einer vorhandenen Anzeigengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="67e61-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="67e61-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67e61-113">EXAMPLES</span></span>

### <span data-ttu-id="67e61-114">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="67e61-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="67e61-115">Fügt den Benutzer mit der Objekt-ID "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" der Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" hinzu.</span><span class="sxs-lookup"><span data-stu-id="67e61-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="67e61-116">Beispiel 2: Hinzufügen eines Benutzers zu einer Gruppe durch Piping</span><span class="sxs-lookup"><span data-stu-id="67e61-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="67e61-117">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Add-AzADGroupMember-Cmdlet weiter, um den Benutzer dieser Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="67e61-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="67e61-118">Beispiel 3: Hinzufügen eines Benutzers zu einer Gruppe nach Prinzipalnamen</span><span class="sxs-lookup"><span data-stu-id="67e61-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="67e61-119">Fügt einen Benutzer zu einer Gruppe hinzu und listet die Mitglieder der Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="67e61-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="67e61-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e61-120">PARAMETERS</span></span>

### <span data-ttu-id="67e61-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e61-121">-DefaultProfile</span></span>
<span data-ttu-id="67e61-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67e61-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e61-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="67e61-123">-MemberObjectId</span></span>
<span data-ttu-id="67e61-124">Die Objekt-ID des Members.</span><span class="sxs-lookup"><span data-stu-id="67e61-124">The object id of the member.</span></span>

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

### <span data-ttu-id="67e61-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="67e61-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="67e61-126">Der UPN der Mitglieder, die der Gruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67e61-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="67e61-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67e61-127">-PassThru</span></span>
<span data-ttu-id="67e61-128">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="67e61-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="67e61-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="67e61-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="67e61-130">Der Anzeigename der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67e61-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="67e61-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="67e61-131">-TargetGroupObject</span></span>
<span data-ttu-id="67e61-132">Die Objektdarstellung der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67e61-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="67e61-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="67e61-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="67e61-134">Die Objekt-ID der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67e61-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="67e61-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67e61-135">-Confirm</span></span>
<span data-ttu-id="67e61-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67e61-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e61-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e61-137">-WhatIf</span></span>
<span data-ttu-id="67e61-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67e61-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e61-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67e61-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e61-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e61-140">CommonParameters</span></span>
<span data-ttu-id="67e61-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e61-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e61-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67e61-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e61-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67e61-143">INPUTS</span></span>

### <span data-ttu-id="67e61-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="67e61-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="67e61-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67e61-145">OUTPUTS</span></span>

### <span data-ttu-id="67e61-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67e61-146">System.Boolean</span></span>

## <span data-ttu-id="67e61-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="67e61-147">NOTES</span></span>

## <span data-ttu-id="67e61-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67e61-148">RELATED LINKS</span></span>
