---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143753"
---
# <span data-ttu-id="75c50-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="75c50-101">Set-AzDefault</span></span>

## <span data-ttu-id="75c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c50-102">SYNOPSIS</span></span>
<span data-ttu-id="75c50-103">Legt einen Standardwert im aktuellen Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="75c50-103">Sets a default in the current context</span></span>

## <span data-ttu-id="75c50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75c50-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c50-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75c50-105">DESCRIPTION</span></span>
<span data-ttu-id="75c50-106">Das Set-AzDefault cmdlet fügt die Standardeinstellungen im aktuellen Kontext hinzu oder ändert sie.</span><span class="sxs-lookup"><span data-stu-id="75c50-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="75c50-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75c50-107">EXAMPLES</span></span>

### <span data-ttu-id="75c50-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75c50-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="75c50-109">Mit diesem Befehl wird die Standardressourcengruppe auf die vom Benutzer angegebene Ressourcengruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="75c50-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="75c50-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c50-110">PARAMETERS</span></span>

### <span data-ttu-id="75c50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c50-111">-DefaultProfile</span></span>
<span data-ttu-id="75c50-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75c50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c50-113">-Force</span><span class="sxs-lookup"><span data-stu-id="75c50-113">-Force</span></span>
<span data-ttu-id="75c50-114">Erstellen einer neuen Ressourcengruppe, wenn der angegebene Standardwert nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="75c50-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="75c50-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c50-115">-ResourceGroupName</span></span>
<span data-ttu-id="75c50-116">Name der Ressourcengruppe, die als Standard festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="75c50-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="75c50-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="75c50-117">-Scope</span></span>
<span data-ttu-id="75c50-118">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="75c50-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="75c50-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75c50-119">-Confirm</span></span>
<span data-ttu-id="75c50-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75c50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c50-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="75c50-121">-WhatIf</span></span>
<span data-ttu-id="75c50-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75c50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c50-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75c50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c50-124">CommonParameters</span></span>
<span data-ttu-id="75c50-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c50-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c50-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c50-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75c50-127">INPUTS</span></span>

### <span data-ttu-id="75c50-128">System.String</span><span class="sxs-lookup"><span data-stu-id="75c50-128">System.String</span></span>

## <span data-ttu-id="75c50-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75c50-129">OUTPUTS</span></span>

### <span data-ttu-id="75c50-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75c50-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="75c50-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75c50-131">NOTES</span></span>

## <span data-ttu-id="75c50-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75c50-132">RELATED LINKS</span></span>
