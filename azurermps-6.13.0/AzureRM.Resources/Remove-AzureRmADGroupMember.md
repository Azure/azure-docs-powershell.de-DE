---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662658"
---
# <span data-ttu-id="15ada-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="15ada-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="15ada-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15ada-102">SYNOPSIS</span></span>
<span data-ttu-id="15ada-103">Entfernt einen Benutzer aus einer Anzeigengruppe.</span><span class="sxs-lookup"><span data-stu-id="15ada-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15ada-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15ada-104">SYNTAX</span></span>

### <span data-ttu-id="15ada-105">ExplicitParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="15ada-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15ada-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="15ada-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ada-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="15ada-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ada-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="15ada-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ada-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ada-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ada-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ada-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ada-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ada-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15ada-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15ada-112">DESCRIPTION</span></span>
<span data-ttu-id="15ada-113">Entfernt einen Benutzer aus einer Anzeigengruppe.</span><span class="sxs-lookup"><span data-stu-id="15ada-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="15ada-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15ada-114">EXAMPLES</span></span>

### <span data-ttu-id="15ada-115">Beispiel 1: Entfernen eines Benutzers aus einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="15ada-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="15ada-116">Entfernt den Benutzer mit der Objekt-ID "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" aus der Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="15ada-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="15ada-117">Beispiel 2 – Entfernen eines Benutzers aus einer Gruppe durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="15ada-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="15ada-118">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Remove-AzureRmADGroupMember-Cmdlet weiter, um den Benutzer zu dieser Gruppe zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="15ada-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="15ada-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="15ada-119">PARAMETERS</span></span>

### <span data-ttu-id="15ada-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ada-120">-DefaultProfile</span></span>
<span data-ttu-id="15ada-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15ada-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ada-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="15ada-122">-GroupDisplayName</span></span>
<span data-ttu-id="15ada-123">Der Anzeigename der Gruppe, aus der die Mitglieder entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15ada-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="15ada-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="15ada-124">-GroupObject</span></span>
<span data-ttu-id="15ada-125">Die Objektdarstellung der Gruppe, aus der das Element entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="15ada-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ada-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="15ada-126">-GroupObjectId</span></span>
<span data-ttu-id="15ada-127">Die Objekt-ID der Gruppe, aus der das Mitglied entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="15ada-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ada-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="15ada-128">-MemberObjectId</span></span>
<span data-ttu-id="15ada-129">Die Objekt-ID des Members.</span><span class="sxs-lookup"><span data-stu-id="15ada-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ada-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="15ada-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="15ada-131">Der UPN der zu entfernenden Member (s).</span><span class="sxs-lookup"><span data-stu-id="15ada-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="15ada-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15ada-132">-PassThru</span></span>
<span data-ttu-id="15ada-133">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="15ada-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="15ada-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15ada-134">-Confirm</span></span>
<span data-ttu-id="15ada-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15ada-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15ada-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15ada-136">-WhatIf</span></span>
<span data-ttu-id="15ada-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15ada-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15ada-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15ada-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15ada-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ada-139">CommonParameters</span></span>
<span data-ttu-id="15ada-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15ada-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ada-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15ada-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ada-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15ada-142">INPUTS</span></span>

### <span data-ttu-id="15ada-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="15ada-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="15ada-144">Parameter: groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="15ada-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="15ada-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15ada-145">OUTPUTS</span></span>

### <span data-ttu-id="15ada-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15ada-146">System.Boolean</span></span>

## <span data-ttu-id="15ada-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="15ada-147">NOTES</span></span>

## <span data-ttu-id="15ada-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15ada-148">RELATED LINKS</span></span>
