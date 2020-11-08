---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175323"
---
# <span data-ttu-id="f396e-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="f396e-101">Clear-AzDefault</span></span>

## <span data-ttu-id="f396e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f396e-102">SYNOPSIS</span></span>
<span data-ttu-id="f396e-103">Löscht die vom Benutzer im aktuellen Kontext festgelegten Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f396e-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="f396e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f396e-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f396e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f396e-105">DESCRIPTION</span></span>
<span data-ttu-id="f396e-106">Das Clear-AzDefault-Cmdlet entfernt die vom Benutzer festgelegten Standardeinstellungen, abhängig von den vom Benutzer angegebenen Schalterparametern.</span><span class="sxs-lookup"><span data-stu-id="f396e-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="f396e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f396e-107">EXAMPLES</span></span>

### <span data-ttu-id="f396e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f396e-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="f396e-109">Mit diesem Befehl werden alle Standardeinstellungen entfernt, die vom Benutzer im aktuellen Kontext gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="f396e-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="f396e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f396e-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="f396e-111">Dieser Befehl entfernt die vom Benutzer im aktuellen Kontext gesetzte Standardressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f396e-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="f396e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f396e-112">PARAMETERS</span></span>

### <span data-ttu-id="f396e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f396e-113">-DefaultProfile</span></span>
<span data-ttu-id="f396e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f396e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f396e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f396e-115">-Force</span></span>
<span data-ttu-id="f396e-116">Entfernen aller Standardeinstellungen, wenn kein Standardwert angegeben ist</span><span class="sxs-lookup"><span data-stu-id="f396e-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="f396e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f396e-117">-PassThru</span></span>
<span data-ttu-id="f396e-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="f396e-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f396e-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f396e-119">-ResourceGroup</span></span>
<span data-ttu-id="f396e-120">Standardressourcen Gruppe löschen</span><span class="sxs-lookup"><span data-stu-id="f396e-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="f396e-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="f396e-121">-Scope</span></span>
<span data-ttu-id="f396e-122">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="f396e-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f396e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f396e-123">-Confirm</span></span>
<span data-ttu-id="f396e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f396e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f396e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f396e-125">-WhatIf</span></span>
<span data-ttu-id="f396e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f396e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f396e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f396e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f396e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f396e-128">CommonParameters</span></span>
<span data-ttu-id="f396e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f396e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f396e-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f396e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f396e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f396e-131">INPUTS</span></span>

### <span data-ttu-id="f396e-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f396e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f396e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f396e-133">OUTPUTS</span></span>

### <span data-ttu-id="f396e-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f396e-134">System.Boolean</span></span>

## <span data-ttu-id="f396e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f396e-135">NOTES</span></span>

## <span data-ttu-id="f396e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f396e-136">RELATED LINKS</span></span>
