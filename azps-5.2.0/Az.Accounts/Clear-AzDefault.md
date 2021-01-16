---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291790"
---
# <span data-ttu-id="8d5de-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="8d5de-101">Clear-AzDefault</span></span>

## <span data-ttu-id="8d5de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5de-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5de-103">Deaktiviert die vom Benutzer im aktuellen Kontext festgelegten Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="8d5de-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="8d5de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d5de-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d5de-105">DESCRIPTION</span></span>
<span data-ttu-id="8d5de-106">Das Clear-AzDefault entfernt die vom Benutzer festgelegten Standardwerte abhängig von den vom Benutzer angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="8d5de-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="8d5de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d5de-107">EXAMPLES</span></span>

### <span data-ttu-id="8d5de-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d5de-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="8d5de-109">Mit diesem Befehl werden alle vom Benutzer im aktuellen Kontext festgelegten Standardeinstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="8d5de-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="8d5de-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8d5de-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="8d5de-111">Mit diesem Befehl wird die vom Benutzer im aktuellen Kontext festgelegte Standardressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="8d5de-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="8d5de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d5de-112">PARAMETERS</span></span>

### <span data-ttu-id="8d5de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5de-113">-DefaultProfile</span></span>
<span data-ttu-id="8d5de-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d5de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d5de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8d5de-115">-Force</span></span>
<span data-ttu-id="8d5de-116">Alle Standardwerte entfernen, wenn kein Standardwert angegeben ist</span><span class="sxs-lookup"><span data-stu-id="8d5de-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="8d5de-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d5de-117">-PassThru</span></span>
<span data-ttu-id="8d5de-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8d5de-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8d5de-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d5de-119">-ResourceGroup</span></span>
<span data-ttu-id="8d5de-120">Löschen der Standardressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8d5de-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="8d5de-121">-Scope</span></span>
<span data-ttu-id="8d5de-122">Bestimmt den Umfang der Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="8d5de-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8d5de-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d5de-123">-Confirm</span></span>
<span data-ttu-id="8d5de-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d5de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5de-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8d5de-125">-WhatIf</span></span>
<span data-ttu-id="8d5de-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d5de-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5de-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d5de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5de-128">CommonParameters</span></span>
<span data-ttu-id="8d5de-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5de-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5de-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5de-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d5de-131">INPUTS</span></span>

### <span data-ttu-id="8d5de-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d5de-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d5de-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d5de-133">OUTPUTS</span></span>

### <span data-ttu-id="8d5de-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d5de-134">System.Boolean</span></span>

## <span data-ttu-id="8d5de-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8d5de-135">NOTES</span></span>

## <span data-ttu-id="8d5de-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8d5de-136">RELATED LINKS</span></span>
