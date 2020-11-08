---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165006"
---
# <span data-ttu-id="c292e-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="c292e-101">Update-AzTag</span></span>

## <span data-ttu-id="c292e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c292e-102">SYNOPSIS</span></span>

<span data-ttu-id="c292e-103">Aktualisiert selektiv die Gruppe von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c292e-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="c292e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c292e-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="c292e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c292e-105">DESCRIPTION</span></span>

<span data-ttu-id="c292e-106">Das Cmdlet " **Update-AzTag** " mit einer Ressourcen-Kennung aktualisiert selektiv die Gruppe von Tags für eine Ressource **oder ein Abonnement** .</span><span class="sxs-lookup"><span data-stu-id="c292e-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="c292e-107">Dieser Vorgang ermöglicht das ersetzen, Zusammenführen oder selektives Löschen von Tags für die angegebene Ressource oder das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c292e-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="c292e-108">Die angegebene Entität kann am Ende des Vorgangs maximal 50-Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="c292e-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="c292e-109">Mit der Option "ersetzen" wird der gesamte Satz vorhandener Tags durch einen neuen Satz ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c292e-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="c292e-110">Mit der Option "Zusammenführen" können Sie Tags mit neuen Namen hinzufügen und die Werte von Tags mit vorhandenen Namen aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c292e-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="c292e-111">Die Option "Löschen" ermöglicht das selektive Löschen von Tags auf der Grundlage von angegebenen Namen oder Name-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="c292e-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="c292e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c292e-112">EXAMPLES</span></span>

### <span data-ttu-id="c292e-113">Beispiel 1: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "Zusammenführen"</span><span class="sxs-lookup"><span data-stu-id="c292e-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="c292e-114">Dieser Befehl führt die Gruppe von Tags im Abonnement mit {subId} zusammen.</span><span class="sxs-lookup"><span data-stu-id="c292e-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c292e-115">Beispiel 2: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "ersetzen"</span><span class="sxs-lookup"><span data-stu-id="c292e-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="c292e-116">Dieser Befehl Repalces den Satz von Tags für das Abonnement mit {subId}.</span><span class="sxs-lookup"><span data-stu-id="c292e-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c292e-117">Beispiel 3: selektives Aktualisieren der Gruppe von Transpondern in einem Abonnement mit dem Vorgang "Löschen"</span><span class="sxs-lookup"><span data-stu-id="c292e-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="c292e-118">Mit diesem Befehl wird der Satz von Tags im Abonnement mit {subId} gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c292e-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="c292e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c292e-119">PARAMETERS</span></span>

### <span data-ttu-id="c292e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c292e-120">-DefaultProfile</span></span>
<span data-ttu-id="c292e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c292e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c292e-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c292e-122">-ResourceId</span></span>
<span data-ttu-id="c292e-123">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="c292e-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="c292e-124">Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.</span><span class="sxs-lookup"><span data-stu-id="c292e-124">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="c292e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c292e-125">-Tag</span></span>
<span data-ttu-id="c292e-126">Die Gruppe von Tags, die für die Aktualisierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c292e-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="c292e-127">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c292e-127">-Operation</span></span>
<span data-ttu-id="c292e-128">Der Aktualisierungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="c292e-128">The update operation.</span></span> <span data-ttu-id="c292e-129">Optionen sind "Zusammenführen", "ersetzen" und "Löschen".</span><span class="sxs-lookup"><span data-stu-id="c292e-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c292e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c292e-130">-Confirm</span></span>
<span data-ttu-id="c292e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c292e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c292e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c292e-132">-WhatIf</span></span>
<span data-ttu-id="c292e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c292e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c292e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c292e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c292e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c292e-135">CommonParameters</span></span>
<span data-ttu-id="c292e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c292e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c292e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c292e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c292e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c292e-138">INPUTS</span></span>

### <span data-ttu-id="c292e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c292e-139">System.String</span></span>

### <span data-ttu-id="c292e-140">Microsoft. Azure. Commands. Tags. Model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="c292e-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="c292e-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c292e-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c292e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c292e-142">OUTPUTS</span></span>

### <span data-ttu-id="c292e-143">Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="c292e-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="c292e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="c292e-144">NOTES</span></span>

## <span data-ttu-id="c292e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c292e-145">RELATED LINKS</span></span>

[<span data-ttu-id="c292e-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="c292e-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="c292e-147">Neu – AzTag</span><span class="sxs-lookup"><span data-stu-id="c292e-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="c292e-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="c292e-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
