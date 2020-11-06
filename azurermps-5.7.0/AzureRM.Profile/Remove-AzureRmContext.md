---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500473"
---
# <span data-ttu-id="b916b-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b916b-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="b916b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b916b-102">SYNOPSIS</span></span>
<span data-ttu-id="b916b-103">Entfernen eines Kontexts aus der Gruppe der verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="b916b-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b916b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b916b-104">SYNTAX</span></span>

### <span data-ttu-id="b916b-105">RemoveByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b916b-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b916b-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="b916b-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="b916b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b916b-107">DESCRIPTION</span></span>
<span data-ttu-id="b916b-108">Entfernen eines Azure-Kontexts aus der Gruppe von Kontexten</span><span class="sxs-lookup"><span data-stu-id="b916b-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="b916b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b916b-109">EXAMPLES</span></span>

### <span data-ttu-id="b916b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b916b-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="b916b-111">Entfernen des Kontexts mit dem Namen "Standard"</span><span class="sxs-lookup"><span data-stu-id="b916b-111">Remove the context named default</span></span>

## <span data-ttu-id="b916b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b916b-112">PARAMETERS</span></span>

### <span data-ttu-id="b916b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b916b-113">-DefaultProfile</span></span>
<span data-ttu-id="b916b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b916b-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b916b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b916b-115">-Force</span></span>
<span data-ttu-id="b916b-116">Entfernen des Kontexts, auch wenn es sich um die defualt handelt</span><span class="sxs-lookup"><span data-stu-id="b916b-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="b916b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b916b-117">-InputObject</span></span>
<span data-ttu-id="b916b-118">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b916b-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b916b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b916b-119">-Name</span></span>
<span data-ttu-id="b916b-120">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="b916b-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b916b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b916b-121">-PassThru</span></span>
<span data-ttu-id="b916b-122">Zurückgeben des entfernten Kontexts</span><span class="sxs-lookup"><span data-stu-id="b916b-122">Return the removed context</span></span>

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

### <span data-ttu-id="b916b-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="b916b-123">-Scope</span></span>
<span data-ttu-id="b916b-124">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="b916b-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b916b-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b916b-125">-Confirm</span></span>
<span data-ttu-id="b916b-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b916b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b916b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b916b-127">-WhatIf</span></span>
<span data-ttu-id="b916b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b916b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b916b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b916b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b916b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b916b-130">CommonParameters</span></span>
<span data-ttu-id="b916b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b916b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b916b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b916b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b916b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b916b-133">INPUTS</span></span>

### <span data-ttu-id="b916b-134">Keine</span><span class="sxs-lookup"><span data-stu-id="b916b-134">None</span></span>

## <span data-ttu-id="b916b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b916b-135">OUTPUTS</span></span>

### <span data-ttu-id="b916b-136">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b916b-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="b916b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="b916b-137">NOTES</span></span>

## <span data-ttu-id="b916b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b916b-138">RELATED LINKS</span></span>

