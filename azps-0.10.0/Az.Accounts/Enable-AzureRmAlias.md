---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 173c78b662253bf347ad5cc30d79208ebe514c15
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841079"
---
# <span data-ttu-id="a2852-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a2852-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="a2852-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2852-102">SYNOPSIS</span></span>
<span data-ttu-id="a2852-103">Aktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="a2852-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="a2852-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2852-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2852-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2852-105">DESCRIPTION</span></span>
<span data-ttu-id="a2852-106">Aktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="a2852-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="a2852-107">Wenn-Module angegeben ist, werden nur in den aufgeführten Modulen Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2852-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="a2852-108">Andernfalls sind alle AzureRm-Aliase aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a2852-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="a2852-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2852-109">EXAMPLES</span></span>

### <span data-ttu-id="a2852-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2852-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="a2852-111">Aktiviert alle AzureRm-Präfixe für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a2852-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="a2852-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2852-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="a2852-113">Aktiviert AzureRm-Aliase für das AZ. Accounts-Modul sowohl für den aktuellen Prozess als auch für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a2852-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="a2852-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2852-114">PARAMETERS</span></span>

### <span data-ttu-id="a2852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2852-115">-DefaultProfile</span></span>
<span data-ttu-id="a2852-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2852-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2852-117">-Module</span><span class="sxs-lookup"><span data-stu-id="a2852-117">-Module</span></span>
<span data-ttu-id="a2852-118">Gibt an, für welche Module Aliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2852-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="a2852-119">Wenn None angegeben wird, ist Standard alle Module.</span><span class="sxs-lookup"><span data-stu-id="a2852-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="a2852-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2852-120">-PassThru</span></span>
<span data-ttu-id="a2852-121">Wenn angegeben, gibt das Cmdlet alle aktivierten Aliase zurück.</span><span class="sxs-lookup"><span data-stu-id="a2852-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="a2852-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="a2852-122">-Scope</span></span>
<span data-ttu-id="a2852-123">Gibt an, für welche Bereichs Aliase aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2852-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="a2852-124">Standard ist "local"</span><span class="sxs-lookup"><span data-stu-id="a2852-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="a2852-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2852-125">-Confirm</span></span>
<span data-ttu-id="a2852-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2852-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2852-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2852-127">-WhatIf</span></span>
<span data-ttu-id="a2852-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2852-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2852-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2852-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2852-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2852-130">CommonParameters</span></span>
<span data-ttu-id="a2852-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2852-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2852-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2852-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2852-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2852-133">INPUTS</span></span>

### <span data-ttu-id="a2852-134">Keine</span><span class="sxs-lookup"><span data-stu-id="a2852-134">None</span></span>

## <span data-ttu-id="a2852-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2852-135">OUTPUTS</span></span>

### <span data-ttu-id="a2852-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a2852-136">System.String</span></span>

## <span data-ttu-id="a2852-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2852-137">NOTES</span></span>

## <span data-ttu-id="a2852-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2852-138">RELATED LINKS</span></span>
