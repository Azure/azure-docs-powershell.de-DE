---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: e87c28627c42d75687569d23a0667f5c403a5def
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841088"
---
# <span data-ttu-id="80d9e-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="80d9e-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="80d9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="80d9e-103">Deaktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="80d9e-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="80d9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80d9e-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="80d9e-106">Deaktiviert AzureRm-Präfix Aliase für AZ-Module.</span><span class="sxs-lookup"><span data-stu-id="80d9e-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="80d9e-107">Wenn-Module angegeben ist, werden nur in den aufgeführten Modulen Aliase deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="80d9e-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="80d9e-108">Andernfalls sind alle AzureRm-Aliase deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="80d9e-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="80d9e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80d9e-109">EXAMPLES</span></span>

### <span data-ttu-id="80d9e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80d9e-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="80d9e-111">Deaktiviert alle AzureRm-Präfixe für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="80d9e-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="80d9e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80d9e-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="80d9e-113">Deaktiviert AzureRm-Aliase für das AZ. Accounts-Modul sowohl für den aktuellen Prozess als auch für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="80d9e-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="80d9e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="80d9e-114">PARAMETERS</span></span>

### <span data-ttu-id="80d9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d9e-115">-DefaultProfile</span></span>
<span data-ttu-id="80d9e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80d9e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d9e-117">-Module</span><span class="sxs-lookup"><span data-stu-id="80d9e-117">-Module</span></span>
<span data-ttu-id="80d9e-118">Gibt an, für welche Module Aliase deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80d9e-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="80d9e-119">Wenn None angegeben wird, ist Standard alle aktivierten Module.</span><span class="sxs-lookup"><span data-stu-id="80d9e-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="80d9e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80d9e-120">-PassThru</span></span>
<span data-ttu-id="80d9e-121">Wenn angegeben, gibt das Cmdlet alle deaktivierten Aliase zurück.</span><span class="sxs-lookup"><span data-stu-id="80d9e-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="80d9e-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="80d9e-122">-Scope</span></span>
<span data-ttu-id="80d9e-123">Gibt an, für welche Bereichs Aliase deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80d9e-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="80d9e-124">Standard ist "Prozess"</span><span class="sxs-lookup"><span data-stu-id="80d9e-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80d9e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80d9e-125">-Confirm</span></span>
<span data-ttu-id="80d9e-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80d9e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d9e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d9e-127">-WhatIf</span></span>
<span data-ttu-id="80d9e-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80d9e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80d9e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80d9e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d9e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d9e-130">CommonParameters</span></span>
<span data-ttu-id="80d9e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d9e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d9e-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d9e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d9e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80d9e-133">INPUTS</span></span>

### <span data-ttu-id="80d9e-134">Keine</span><span class="sxs-lookup"><span data-stu-id="80d9e-134">None</span></span>

## <span data-ttu-id="80d9e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80d9e-135">OUTPUTS</span></span>

### <span data-ttu-id="80d9e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="80d9e-136">System.String</span></span>

## <span data-ttu-id="80d9e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="80d9e-137">NOTES</span></span>

## <span data-ttu-id="80d9e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80d9e-138">RELATED LINKS</span></span>
