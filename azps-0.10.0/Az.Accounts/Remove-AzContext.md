---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: accea2f11e00cecf3771e87e14a42a446a75367d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841040"
---
# <span data-ttu-id="5cdc1-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="5cdc1-101">Remove-AzContext</span></span>

## <span data-ttu-id="5cdc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdc1-103">Entfernen eines Kontexts aus der Gruppe der verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="5cdc1-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="5cdc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cdc1-104">SYNTAX</span></span>

### <span data-ttu-id="5cdc1-105">RemoveByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cdc1-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cdc1-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="5cdc1-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="5cdc1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cdc1-107">DESCRIPTION</span></span>
<span data-ttu-id="5cdc1-108">Entfernen eines Azure-Kontexts aus der Gruppe von Kontexten</span><span class="sxs-lookup"><span data-stu-id="5cdc1-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="5cdc1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cdc1-109">EXAMPLES</span></span>

### <span data-ttu-id="5cdc1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cdc1-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="5cdc1-111">Entfernen des Kontexts mit dem Namen "Standard"</span><span class="sxs-lookup"><span data-stu-id="5cdc1-111">Remove the context named default</span></span>

## <span data-ttu-id="5cdc1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cdc1-112">PARAMETERS</span></span>

### <span data-ttu-id="5cdc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdc1-113">-DefaultProfile</span></span>
<span data-ttu-id="5cdc1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cdc1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5cdc1-115">-Force</span></span>
<span data-ttu-id="5cdc1-116">Entfernen des Kontexts, auch wenn dies der Standardwert ist</span><span class="sxs-lookup"><span data-stu-id="5cdc1-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="5cdc1-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5cdc1-117">-InputObject</span></span>
<span data-ttu-id="5cdc1-118">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5cdc1-119">-Name</span></span>
<span data-ttu-id="5cdc1-120">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="5cdc1-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdc1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cdc1-121">-PassThru</span></span>
<span data-ttu-id="5cdc1-122">Zurückgeben des entfernten Kontexts</span><span class="sxs-lookup"><span data-stu-id="5cdc1-122">Return the removed context</span></span>

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

### <span data-ttu-id="5cdc1-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="5cdc1-123">-Scope</span></span>
<span data-ttu-id="5cdc1-124">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="5cdc1-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cdc1-125">-Confirm</span></span>
<span data-ttu-id="5cdc1-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cdc1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cdc1-127">-WhatIf</span></span>
<span data-ttu-id="5cdc1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cdc1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cdc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdc1-130">CommonParameters</span></span>
<span data-ttu-id="5cdc1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cdc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdc1-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cdc1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdc1-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cdc1-133">INPUTS</span></span>

### <span data-ttu-id="5cdc1-134">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5cdc1-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="5cdc1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cdc1-135">OUTPUTS</span></span>

### <span data-ttu-id="5cdc1-136">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5cdc1-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="5cdc1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cdc1-137">NOTES</span></span>

## <span data-ttu-id="5cdc1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cdc1-138">RELATED LINKS</span></span>
