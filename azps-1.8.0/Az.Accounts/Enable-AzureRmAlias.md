---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 24862931e19d0e8b8c7b8568aabb6f25cf65f9c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650506"
---
# <span data-ttu-id="195f8-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="195f8-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="195f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="195f8-102">SYNOPSIS</span></span>
<span data-ttu-id="195f8-103">Aktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="195f8-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="195f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="195f8-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="195f8-105">DESCRIPTION</span></span>
<span data-ttu-id="195f8-106">Aktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="195f8-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="195f8-107">Wenn-Module angegeben ist, werden nur in den aufgeführten Modulen Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="195f8-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="195f8-108">Andernfalls sind alle AzureRm-Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="195f8-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="195f8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="195f8-109">EXAMPLES</span></span>

### <span data-ttu-id="195f8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="195f8-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="195f8-111">Aktiviert alle AzureRm-Präfixe für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="195f8-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="195f8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="195f8-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="195f8-113">Aktiviert AzureRm-Aliase für das AZ. Accounts-Modul sowohl für den aktuellen Prozess als auch für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="195f8-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="195f8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="195f8-114">PARAMETERS</span></span>

### <span data-ttu-id="195f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195f8-115">-DefaultProfile</span></span>
<span data-ttu-id="195f8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="195f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="195f8-117">-Module</span><span class="sxs-lookup"><span data-stu-id="195f8-117">-Module</span></span>
<span data-ttu-id="195f8-118">Gibt an, für welche Module Aliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="195f8-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="195f8-119">Wenn None angegeben wird, ist Standard alle Module.</span><span class="sxs-lookup"><span data-stu-id="195f8-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="195f8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="195f8-120">-PassThru</span></span>
<span data-ttu-id="195f8-121">Wenn angegeben, gibt das Cmdlet alle aktivierten Aliase zurück.</span><span class="sxs-lookup"><span data-stu-id="195f8-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="195f8-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="195f8-122">-Scope</span></span>
<span data-ttu-id="195f8-123">Gibt an, für welche Bereichs Aliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="195f8-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="195f8-124">Standard ist "local"</span><span class="sxs-lookup"><span data-stu-id="195f8-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="195f8-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="195f8-125">-Confirm</span></span>
<span data-ttu-id="195f8-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="195f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195f8-127">-WhatIf</span></span>
<span data-ttu-id="195f8-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="195f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195f8-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="195f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195f8-130">CommonParameters</span></span>
<span data-ttu-id="195f8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195f8-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195f8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195f8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="195f8-133">INPUTS</span></span>

### <span data-ttu-id="195f8-134">Keine</span><span class="sxs-lookup"><span data-stu-id="195f8-134">None</span></span>

## <span data-ttu-id="195f8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="195f8-135">OUTPUTS</span></span>

### <span data-ttu-id="195f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="195f8-136">System.String</span></span>

## <span data-ttu-id="195f8-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="195f8-137">NOTES</span></span>

## <span data-ttu-id="195f8-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="195f8-138">RELATED LINKS</span></span>
