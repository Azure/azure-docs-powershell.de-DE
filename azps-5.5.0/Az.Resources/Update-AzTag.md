---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145913"
---
# <span data-ttu-id="71128-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="71128-101">Update-AzTag</span></span>

## <span data-ttu-id="71128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71128-102">SYNOPSIS</span></span>

<span data-ttu-id="71128-103">Aktualisiert die Gruppe von Tags für eine Ressource oder ein Abonnement selektiv.</span><span class="sxs-lookup"><span data-stu-id="71128-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="71128-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71128-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="71128-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71128-105">DESCRIPTION</span></span>

<span data-ttu-id="71128-106">Das **Cmdlet "Update-AzTag"** mit einer **"ResourceId"** aktualisiert selektiv die Markierungen einer Ressource oder eines Abonnements.</span><span class="sxs-lookup"><span data-stu-id="71128-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="71128-107">Dieser Vorgang ermöglicht das Ersetzen, Zusammenführen oder selektive Löschen von Tags für die angegebene Ressource oder das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71128-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="71128-108">Die angegebene Entität kann am Ende des Vorgangs maximal 50 Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="71128-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="71128-109">Die Option "Ersetzen" ersetzt den gesamten Satz vorhandener Tags durch einen neuen Satz.</span><span class="sxs-lookup"><span data-stu-id="71128-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="71128-110">Die Option "Zusammenführen" ermöglicht das Hinzufügen von Tags mit neuen Namen und das Aktualisieren der Werte von Tags mit vorhandenen Namen.</span><span class="sxs-lookup"><span data-stu-id="71128-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="71128-111">Die Option "Löschen" ermöglicht das selektive Löschen von Tags basierend auf bestimmten Namen oder Name/Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="71128-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="71128-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71128-112">EXAMPLES</span></span>

### <span data-ttu-id="71128-113">Beispiel 1: Selektives Aktualisieren der Gruppe von Markierungen in einem Abonnement mit "Zusammenführen"-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71128-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="71128-114">Mit diesem Befehl werden die Markierungen im Abonnement mit {subId} zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="71128-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="71128-115">Beispiel 2: Selektives Aktualisieren der Gruppe von Tags in einem Abonnement durch "Ersetzen"-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71128-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="71128-116">Mit diesem Befehl wird die Gruppe von Tags für das Abonnement mit {subId} erneut umschalten.</span><span class="sxs-lookup"><span data-stu-id="71128-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="71128-117">Beispiel 3: Selektives Aktualisieren der Gruppe von Markierungen in einem Abonnement mit "Löschvorgang"</span><span class="sxs-lookup"><span data-stu-id="71128-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="71128-118">Mit diesem Befehl wird die Gruppe von Tags für das Abonnement mit {subId} gelöscht.</span><span class="sxs-lookup"><span data-stu-id="71128-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="71128-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71128-119">PARAMETERS</span></span>

### <span data-ttu-id="71128-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71128-120">-DefaultProfile</span></span>
<span data-ttu-id="71128-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71128-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71128-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71128-122">-ResourceId</span></span>
<span data-ttu-id="71128-123">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="71128-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="71128-124">Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.</span><span class="sxs-lookup"><span data-stu-id="71128-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71128-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="71128-125">-Tag</span></span>
<span data-ttu-id="71128-126">Die Gruppe von Tags, die für die Aktualisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71128-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71128-127">-Operation</span><span class="sxs-lookup"><span data-stu-id="71128-127">-Operation</span></span>
<span data-ttu-id="71128-128">Der Aktualisierungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="71128-128">The update operation.</span></span> <span data-ttu-id="71128-129">Die Optionen sind "Zusammenführen", "Ersetzen" und "Löschen".</span><span class="sxs-lookup"><span data-stu-id="71128-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71128-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71128-130">-Confirm</span></span>
<span data-ttu-id="71128-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71128-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71128-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71128-132">-WhatIf</span></span>
<span data-ttu-id="71128-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71128-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71128-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71128-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71128-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71128-135">CommonParameters</span></span>
<span data-ttu-id="71128-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71128-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71128-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71128-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71128-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71128-138">INPUTS</span></span>

### <span data-ttu-id="71128-139">System.String</span><span class="sxs-lookup"><span data-stu-id="71128-139">System.String</span></span>

### <span data-ttu-id="71128-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="71128-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="71128-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="71128-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71128-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71128-142">OUTPUTS</span></span>

### <span data-ttu-id="71128-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="71128-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="71128-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71128-144">NOTES</span></span>

## <span data-ttu-id="71128-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71128-145">RELATED LINKS</span></span>

[<span data-ttu-id="71128-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="71128-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="71128-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="71128-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="71128-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="71128-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
