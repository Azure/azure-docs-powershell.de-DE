---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 6163602d2975a9ec77e572ec0033ef2c626d2cfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500470"
---
# <span data-ttu-id="5074a-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5074a-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="5074a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5074a-102">SYNOPSIS</span></span>
<span data-ttu-id="5074a-103">Umbenennen eines Azure-Kontexts</span><span class="sxs-lookup"><span data-stu-id="5074a-103">Rename an Azure context.</span></span>  <span data-ttu-id="5074a-104">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="5074a-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5074a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5074a-105">SYNTAX</span></span>

### <span data-ttu-id="5074a-106">RenameByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="5074a-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="5074a-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="5074a-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="5074a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5074a-108">DESCRIPTION</span></span>
<span data-ttu-id="5074a-109">Umbenennen eines Azure-Kontexts</span><span class="sxs-lookup"><span data-stu-id="5074a-109">Rename an Azure context.</span></span>  <span data-ttu-id="5074a-110">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="5074a-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="5074a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5074a-111">EXAMPLES</span></span>

### <span data-ttu-id="5074a-112">Umbenennen eines Kontexts mithilfe benannter Parameter</span><span class="sxs-lookup"><span data-stu-id="5074a-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="5074a-113">Benennen Sie den Kontext für " user1@contoso.org " mit dem Abonnement "12345-6789-2345-3567890" auf "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="5074a-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="5074a-114">Nach diesem Befehl können Sie den Kontext mit "Select-AzureRmContext work" abgleichen.</span><span class="sxs-lookup"><span data-stu-id="5074a-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="5074a-115">Beachten Sie, dass Sie die Werte für "SourceName" mit Tab-Vervollständigung durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="5074a-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="5074a-116">Umbenennen eines Kontexts mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="5074a-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="5074a-117">Benennen Sie den Kontext mit dem Namen "mein Kontext" auf "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="5074a-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="5074a-118">Nach diesem Befehl können Sie den Kontext mithilfe Select-AzureRmContext Arbeit als Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="5074a-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="5074a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5074a-119">PARAMETERS</span></span>

### <span data-ttu-id="5074a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5074a-120">-DefaultProfile</span></span>
<span data-ttu-id="5074a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="5074a-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5074a-122">-Force</span></span>
<span data-ttu-id="5074a-123">Umbenennen des Kontexts, auch wenn der Zielkontext bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="5074a-123">Rename the context even if the target context already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5074a-124">-InputObject</span></span>
<span data-ttu-id="5074a-125">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5074a-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RenameByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5074a-126">-PassThru</span></span>
<span data-ttu-id="5074a-127">Gibt den umbenannten Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="5074a-127">Return the renamed context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="5074a-128">-Scope</span></span>
<span data-ttu-id="5074a-129">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="5074a-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="5074a-130">-SourceName</span></span>
<span data-ttu-id="5074a-131">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="5074a-131">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RenameByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-132">-Zielname</span><span class="sxs-lookup"><span data-stu-id="5074a-132">-TargetName</span></span>
<span data-ttu-id="5074a-133">Der neue Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="5074a-133">The new name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5074a-134">-Confirm</span></span>
<span data-ttu-id="5074a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5074a-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5074a-136">-WhatIf</span></span>
<span data-ttu-id="5074a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5074a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5074a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5074a-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5074a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5074a-139">CommonParameters</span></span>
<span data-ttu-id="5074a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5074a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5074a-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5074a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5074a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5074a-142">INPUTS</span></span>

### <span data-ttu-id="5074a-143">Keine</span><span class="sxs-lookup"><span data-stu-id="5074a-143">None</span></span>

## <span data-ttu-id="5074a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5074a-144">OUTPUTS</span></span>

### <span data-ttu-id="5074a-145">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5074a-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="5074a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="5074a-146">NOTES</span></span>

## <span data-ttu-id="5074a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5074a-147">RELATED LINKS</span></span>

