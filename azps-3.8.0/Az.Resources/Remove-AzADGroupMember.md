---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 23fa2a476c831216c93796e52267da68debab971
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995503"
---
# <span data-ttu-id="7945c-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7945c-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="7945c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7945c-102">SYNOPSIS</span></span>
<span data-ttu-id="7945c-103">Entfernt einen Benutzer aus einer Anzeigengruppe.</span><span class="sxs-lookup"><span data-stu-id="7945c-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="7945c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7945c-104">SYNTAX</span></span>

### <span data-ttu-id="7945c-105">ExplicitParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7945c-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7945c-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7945c-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7945c-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="7945c-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7945c-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7945c-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7945c-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7945c-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7945c-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7945c-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7945c-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7945c-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7945c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7945c-112">DESCRIPTION</span></span>
<span data-ttu-id="7945c-113">Entfernt einen Benutzer aus einer Anzeigengruppe.</span><span class="sxs-lookup"><span data-stu-id="7945c-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="7945c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7945c-114">EXAMPLES</span></span>

### <span data-ttu-id="7945c-115">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="7945c-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="7945c-116">Entfernt den Benutzer mit der Objekt-ID "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" aus der Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="7945c-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7945c-117">Beispiel 2 – Entfernen eines Benutzers aus einer Gruppe durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="7945c-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="7945c-118">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Remove-AzADGroupMember-Cmdlet weiter, um den Benutzer zu dieser Gruppe zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7945c-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="7945c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="7945c-119">PARAMETERS</span></span>

### <span data-ttu-id="7945c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7945c-120">-DefaultProfile</span></span>
<span data-ttu-id="7945c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7945c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7945c-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7945c-122">-GroupDisplayName</span></span>
<span data-ttu-id="7945c-123">Der Anzeigename der Gruppe, aus der die Mitglieder entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7945c-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="7945c-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="7945c-124">-GroupObject</span></span>
<span data-ttu-id="7945c-125">Die Objektdarstellung der Gruppe, aus der das Element entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7945c-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="7945c-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7945c-126">-GroupObjectId</span></span>
<span data-ttu-id="7945c-127">Die Objekt-ID der Gruppe, aus der das Mitglied entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7945c-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="7945c-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="7945c-128">-MemberObjectId</span></span>
<span data-ttu-id="7945c-129">Die Objekt-ID des Members.</span><span class="sxs-lookup"><span data-stu-id="7945c-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7945c-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7945c-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="7945c-131">Der UPN der zu entfernenden Member (s).</span><span class="sxs-lookup"><span data-stu-id="7945c-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="7945c-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7945c-132">-PassThru</span></span>
<span data-ttu-id="7945c-133">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7945c-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7945c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7945c-134">-Confirm</span></span>
<span data-ttu-id="7945c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7945c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7945c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7945c-136">-WhatIf</span></span>
<span data-ttu-id="7945c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7945c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7945c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7945c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7945c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7945c-139">CommonParameters</span></span>
<span data-ttu-id="7945c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7945c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7945c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7945c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7945c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7945c-142">INPUTS</span></span>

### <span data-ttu-id="7945c-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="7945c-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="7945c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7945c-144">OUTPUTS</span></span>

### <span data-ttu-id="7945c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7945c-145">System.Boolean</span></span>

## <span data-ttu-id="7945c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="7945c-146">NOTES</span></span>

## <span data-ttu-id="7945c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7945c-147">RELATED LINKS</span></span>
