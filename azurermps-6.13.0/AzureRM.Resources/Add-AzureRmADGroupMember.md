---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480141"
---
# <span data-ttu-id="cb721-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="cb721-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="cb721-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb721-102">SYNOPSIS</span></span>
<span data-ttu-id="cb721-103">Fügt einen Benutzer zu einer vorhandenen Anzeigengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb721-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb721-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb721-104">SYNTAX</span></span>

### <span data-ttu-id="cb721-105">MemberObjectIdWithGroupObjectId (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb721-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb721-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="cb721-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb721-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="cb721-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb721-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb721-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb721-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb721-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb721-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb721-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb721-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb721-111">DESCRIPTION</span></span>
<span data-ttu-id="cb721-112">Fügt einen Benutzer zu einer vorhandenen Anzeigengruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb721-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="cb721-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb721-113">EXAMPLES</span></span>

### <span data-ttu-id="cb721-114">Beispiel 1: Hinzufügen eines Benutzers zu einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="cb721-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="cb721-115">Fügt den Benutzer mit der Objekt-ID "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" der Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb721-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="cb721-116">Beispiel 2 – Hinzufügen eines Benutzers zu einer Gruppe durch Verrohrung</span><span class="sxs-lookup"><span data-stu-id="cb721-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="cb721-117">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Add-AzureRmADGroupMember-Cmdlet weiter, um den Benutzer dieser Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cb721-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="cb721-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb721-118">PARAMETERS</span></span>

### <span data-ttu-id="cb721-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb721-119">-DefaultProfile</span></span>
<span data-ttu-id="cb721-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb721-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb721-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="cb721-121">-MemberObjectId</span></span>
<span data-ttu-id="cb721-122">Die Objekt-ID des Members.</span><span class="sxs-lookup"><span data-stu-id="cb721-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb721-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cb721-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="cb721-124">Der UPN der Mitglieder, die der Gruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb721-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="cb721-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb721-125">-PassThru</span></span>
<span data-ttu-id="cb721-126">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="cb721-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cb721-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="cb721-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="cb721-128">Der Anzeigename der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb721-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="cb721-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="cb721-129">-TargetGroupObject</span></span>
<span data-ttu-id="cb721-130">Die Objektdarstellung der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb721-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="cb721-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="cb721-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="cb721-132">Die Objekt-ID der Gruppe, der die Mitglieder hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb721-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="cb721-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb721-133">-Confirm</span></span>
<span data-ttu-id="cb721-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb721-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb721-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb721-135">-WhatIf</span></span>
<span data-ttu-id="cb721-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb721-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb721-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb721-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb721-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb721-138">CommonParameters</span></span>
<span data-ttu-id="cb721-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb721-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb721-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb721-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb721-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb721-141">INPUTS</span></span>

### <span data-ttu-id="cb721-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cb721-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="cb721-143">Parameter: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb721-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="cb721-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb721-144">OUTPUTS</span></span>

### <span data-ttu-id="cb721-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb721-145">System.Boolean</span></span>

## <span data-ttu-id="cb721-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb721-146">NOTES</span></span>

## <span data-ttu-id="cb721-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb721-147">RELATED LINKS</span></span>
