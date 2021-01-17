---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471596"
---
# <span data-ttu-id="bb8d7-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="bb8d7-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="bb8d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8d7-103">Aktiviert AzureRm-Präfixaliase für Az-Module.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="bb8d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb8d7-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb8d7-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8d7-106">Aktiviert AzureRm-Präfixaliase für Az-Module.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="bb8d7-107">Wenn "-Module" angegeben ist, sind für nur aufgelistete Module Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="bb8d7-108">Andernfalls sind alle AzureRm-Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="bb8d7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb8d7-109">EXAMPLES</span></span>

### <span data-ttu-id="bb8d7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb8d7-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="bb8d7-111">Aktiviert alle AzureRm-Präfixe für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="bb8d7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb8d7-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="bb8d7-113">Aktiviert AzureRm-Aliase für das Modul "Az.Accounts" sowohl für den aktuellen Prozess als auch für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="bb8d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb8d7-114">PARAMETERS</span></span>

### <span data-ttu-id="bb8d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8d7-115">-DefaultProfile</span></span>
<span data-ttu-id="bb8d7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb8d7-117">-Module</span><span class="sxs-lookup"><span data-stu-id="bb8d7-117">-Module</span></span>
<span data-ttu-id="bb8d7-118">Gibt an, für welche Module Aliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="bb8d7-119">Wenn keines angegeben wird, ist der Standardwert alle Module.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-119">If none are specified, default is all modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8d7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb8d7-120">-PassThru</span></span>
<span data-ttu-id="bb8d7-121">Falls angegeben, gibt das Cmdlet alle aktivierten Aliase zurück.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="bb8d7-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="bb8d7-122">-Scope</span></span>
<span data-ttu-id="bb8d7-123">Gibt an, für welche Bereichsaliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="bb8d7-124">Der Standardwert ist "Local".</span><span class="sxs-lookup"><span data-stu-id="bb8d7-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8d7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb8d7-125">-Confirm</span></span>
<span data-ttu-id="bb8d7-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8d7-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb8d7-127">-WhatIf</span></span>
<span data-ttu-id="bb8d7-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8d7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8d7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8d7-130">CommonParameters</span></span>
<span data-ttu-id="bb8d7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8d7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8d7-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8d7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8d7-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8d7-133">INPUTS</span></span>

### <span data-ttu-id="bb8d7-134">Keine</span><span class="sxs-lookup"><span data-stu-id="bb8d7-134">None</span></span>

## <span data-ttu-id="bb8d7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb8d7-135">OUTPUTS</span></span>

### <span data-ttu-id="bb8d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bb8d7-136">System.String</span></span>

## <span data-ttu-id="bb8d7-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb8d7-137">NOTES</span></span>

## <span data-ttu-id="bb8d7-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb8d7-138">RELATED LINKS</span></span>
