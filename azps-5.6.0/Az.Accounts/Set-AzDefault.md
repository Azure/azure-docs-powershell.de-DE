---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947664"
---
# <span data-ttu-id="8cf75-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="8cf75-101">Set-AzDefault</span></span>

## <span data-ttu-id="8cf75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf75-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf75-103">Festlegen einer Standardeinstellung im aktuellen Kontext</span><span class="sxs-lookup"><span data-stu-id="8cf75-103">Sets a default in the current context</span></span>

## <span data-ttu-id="8cf75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cf75-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cf75-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf75-106">Das Set-AzDefault-Cmdlet fügt die Standardwerte im aktuellen Kontext hinzu oder ändert sie.</span><span class="sxs-lookup"><span data-stu-id="8cf75-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="8cf75-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cf75-107">EXAMPLES</span></span>

### <span data-ttu-id="8cf75-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cf75-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="8cf75-109">Mit diesem Befehl wird die Standardressourcengruppe auf die vom Benutzer angegebene Ressourcengruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cf75-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="8cf75-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8cf75-110">PARAMETERS</span></span>

### <span data-ttu-id="8cf75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf75-111">-DefaultProfile</span></span>
<span data-ttu-id="8cf75-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cf75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cf75-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8cf75-113">-Force</span></span>
<span data-ttu-id="8cf75-114">Erstellen einer neuen Ressourcengruppe, wenn keine angegebene Standardeinstellung vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="8cf75-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="8cf75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf75-115">-ResourceGroupName</span></span>
<span data-ttu-id="8cf75-116">Name der Als Standard festgelegten Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8cf75-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf75-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="8cf75-117">-Scope</span></span>
<span data-ttu-id="8cf75-118">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="8cf75-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8cf75-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8cf75-119">-Confirm</span></span>
<span data-ttu-id="8cf75-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cf75-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf75-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf75-121">-WhatIf</span></span>
<span data-ttu-id="8cf75-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cf75-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf75-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cf75-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf75-124">CommonParameters</span></span>
<span data-ttu-id="8cf75-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf75-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cf75-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf75-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cf75-127">INPUTS</span></span>

### <span data-ttu-id="8cf75-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8cf75-128">System.String</span></span>

## <span data-ttu-id="8cf75-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cf75-129">OUTPUTS</span></span>

### <span data-ttu-id="8cf75-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cf75-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="8cf75-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8cf75-131">NOTES</span></span>

## <span data-ttu-id="8cf75-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8cf75-132">RELATED LINKS</span></span>
