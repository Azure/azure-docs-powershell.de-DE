---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b54cfdc68c1f6c400decdac9a1ef0f49823a1712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650524"
---
# <span data-ttu-id="53fa7-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="53fa7-101">Clear-AzContext</span></span>

## <span data-ttu-id="53fa7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="53fa7-103">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="53fa7-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="53fa7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53fa7-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53fa7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="53fa7-106">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="53fa7-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="53fa7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53fa7-107">EXAMPLES</span></span>

### <span data-ttu-id="53fa7-108">Globaler Kontext löschen</span><span class="sxs-lookup"><span data-stu-id="53fa7-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="53fa7-109">Entfernen Sie alle Konto-, Abonnement-und Anmeldeinformationen für eine beliebige PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="53fa7-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="53fa7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53fa7-110">PARAMETERS</span></span>

### <span data-ttu-id="53fa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53fa7-111">-DefaultProfile</span></span>
<span data-ttu-id="53fa7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="53fa7-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53fa7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="53fa7-113">-Force</span></span>
<span data-ttu-id="53fa7-114">Löschen aller Benutzer und Gruppen aus dem globalen Bereich ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="53fa7-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="53fa7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53fa7-115">-PassThru</span></span>
<span data-ttu-id="53fa7-116">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="53fa7-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="53fa7-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="53fa7-117">-Scope</span></span>
<span data-ttu-id="53fa7-118">Löschen Sie den Kontext nur für die aktuelle PowerShell-Sitzung oder für alle Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="53fa7-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="53fa7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53fa7-119">-Confirm</span></span>
<span data-ttu-id="53fa7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53fa7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53fa7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53fa7-121">-WhatIf</span></span>
<span data-ttu-id="53fa7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53fa7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53fa7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53fa7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53fa7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fa7-124">CommonParameters</span></span>
<span data-ttu-id="53fa7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53fa7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fa7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53fa7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fa7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53fa7-127">INPUTS</span></span>

### <span data-ttu-id="53fa7-128">Keine</span><span class="sxs-lookup"><span data-stu-id="53fa7-128">None</span></span>

## <span data-ttu-id="53fa7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53fa7-129">OUTPUTS</span></span>

### <span data-ttu-id="53fa7-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53fa7-130">System.Boolean</span></span>

## <span data-ttu-id="53fa7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="53fa7-131">NOTES</span></span>

## <span data-ttu-id="53fa7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53fa7-132">RELATED LINKS</span></span>
