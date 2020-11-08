---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996700"
---
# <span data-ttu-id="57f11-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="57f11-101">Select-AzContext</span></span>

## <span data-ttu-id="57f11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57f11-102">SYNOPSIS</span></span>
<span data-ttu-id="57f11-103">Wählen Sie ein Abonnement und ein Konto für das Ziel in Azure PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="57f11-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="57f11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f11-104">SYNTAX</span></span>

### <span data-ttu-id="57f11-105">SelectByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="57f11-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f11-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="57f11-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="57f11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57f11-107">DESCRIPTION</span></span>
<span data-ttu-id="57f11-108">Wählen Sie in Azure PowerShell-Cmdlets ein Abonnement für Target (oder Konto oder Mandant) aus.</span><span class="sxs-lookup"><span data-stu-id="57f11-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="57f11-109">Nach diesem Cmdlet werden zukünftige Cmdlets auf den ausgewählten Kontext ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="57f11-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="57f11-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57f11-110">EXAMPLES</span></span>

### <span data-ttu-id="57f11-111">Beispiel 1: Ziel eines benannten Kontexts</span><span class="sxs-lookup"><span data-stu-id="57f11-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="57f11-112">Ziel der zukünftigen Azure PowerShell-Cmdlets für das Konto, den Mandanten und das Abonnement im Kontext "Arbeit".</span><span class="sxs-lookup"><span data-stu-id="57f11-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="57f11-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f11-113">PARAMETERS</span></span>

### <span data-ttu-id="57f11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f11-114">-DefaultProfile</span></span>
<span data-ttu-id="57f11-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="57f11-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57f11-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57f11-116">-InputObject</span></span>
<span data-ttu-id="57f11-117">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="57f11-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57f11-118">-Name</span><span class="sxs-lookup"><span data-stu-id="57f11-118">-Name</span></span>
<span data-ttu-id="57f11-119">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="57f11-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f11-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="57f11-120">-Scope</span></span>
<span data-ttu-id="57f11-121">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="57f11-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="57f11-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="57f11-122">-Confirm</span></span>
<span data-ttu-id="57f11-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="57f11-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f11-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f11-124">-WhatIf</span></span>
<span data-ttu-id="57f11-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="57f11-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f11-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="57f11-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f11-127">CommonParameters</span></span>
<span data-ttu-id="57f11-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f11-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f11-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f11-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57f11-130">INPUTS</span></span>

### <span data-ttu-id="57f11-131">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="57f11-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="57f11-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57f11-132">OUTPUTS</span></span>

### <span data-ttu-id="57f11-133">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="57f11-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="57f11-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="57f11-134">NOTES</span></span>

## <span data-ttu-id="57f11-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57f11-135">RELATED LINKS</span></span>
