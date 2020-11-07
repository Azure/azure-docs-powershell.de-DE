---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665006"
---
# <span data-ttu-id="c8353-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c8353-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="c8353-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8353-102">SYNOPSIS</span></span>
<span data-ttu-id="c8353-103">Umbenennen eines Azure-Kontexts</span><span class="sxs-lookup"><span data-stu-id="c8353-103">Rename an Azure context.</span></span>  <span data-ttu-id="c8353-104">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="c8353-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8353-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8353-105">SYNTAX</span></span>

### <span data-ttu-id="c8353-106">Eingabeobjekt (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8353-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="c8353-107">Kontext Name</span><span class="sxs-lookup"><span data-stu-id="c8353-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="c8353-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8353-108">DESCRIPTION</span></span>
<span data-ttu-id="c8353-109">Umbenennen eines Azure-Kontexts</span><span class="sxs-lookup"><span data-stu-id="c8353-109">Rename an Azure context.</span></span>  <span data-ttu-id="c8353-110">Standardmäßig werden Kontexte nach Benutzerkonto und Abonnement benannt.</span><span class="sxs-lookup"><span data-stu-id="c8353-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="c8353-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8353-111">EXAMPLES</span></span>

### <span data-ttu-id="c8353-112">Umbenennen eines Kontexts mithilfe benannter Parameter</span><span class="sxs-lookup"><span data-stu-id="c8353-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="c8353-113">Benennen Sie den Kontext für " user1@contoso.org " mit dem Abonnement "12345-6789-2345-3567890" auf "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="c8353-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="c8353-114">Nach diesem Befehl können Sie den Kontext mit "Select-AzureRmContext work" abgleichen.</span><span class="sxs-lookup"><span data-stu-id="c8353-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="c8353-115">Beachten Sie, dass Sie die Werte für "SourceName" mit Tab-Vervollständigung durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="c8353-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="c8353-116">Umbenennen eines Kontexts mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="c8353-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="c8353-117">Benennen Sie den Kontext mit dem Namen "mein Kontext" auf "Arbeit" um.</span><span class="sxs-lookup"><span data-stu-id="c8353-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="c8353-118">Nach diesem Befehl können Sie den Kontext mithilfe Select-AzureRmContext Arbeit als Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8353-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="c8353-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8353-119">PARAMETERS</span></span>

### <span data-ttu-id="c8353-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8353-120">-DefaultProfile</span></span>
<span data-ttu-id="c8353-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="c8353-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8353-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c8353-122">-Force</span></span>
<span data-ttu-id="c8353-123">Umbenennen des Kontexts, auch wenn der Zielkontext bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="c8353-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="c8353-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8353-124">-InputObject</span></span>
<span data-ttu-id="c8353-125">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8353-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8353-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8353-126">-PassThru</span></span>
<span data-ttu-id="c8353-127">Gibt den umbenannten Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="c8353-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="c8353-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="c8353-128">-Scope</span></span>
<span data-ttu-id="c8353-129">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="c8353-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8353-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="c8353-130">-SourceName</span></span>
<span data-ttu-id="c8353-131">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="c8353-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8353-132">-Zielname</span><span class="sxs-lookup"><span data-stu-id="c8353-132">-TargetName</span></span>
<span data-ttu-id="c8353-133">Der neue Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="c8353-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8353-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8353-134">-Confirm</span></span>
<span data-ttu-id="c8353-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8353-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8353-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8353-136">-WhatIf</span></span>
<span data-ttu-id="c8353-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8353-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8353-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8353-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8353-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8353-139">CommonParameters</span></span>
<span data-ttu-id="c8353-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8353-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8353-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8353-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8353-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8353-142">INPUTS</span></span>

### <span data-ttu-id="c8353-143">Keine</span><span class="sxs-lookup"><span data-stu-id="c8353-143">None</span></span>

## <span data-ttu-id="c8353-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8353-144">OUTPUTS</span></span>

### <span data-ttu-id="c8353-145">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c8353-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="c8353-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8353-146">NOTES</span></span>

## <span data-ttu-id="c8353-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8353-147">RELATED LINKS</span></span>

