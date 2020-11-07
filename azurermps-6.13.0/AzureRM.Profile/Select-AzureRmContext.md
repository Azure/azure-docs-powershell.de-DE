---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 86d236a3601dfac9467b5da01cd297255ac98312
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663345"
---
# <span data-ttu-id="281e4-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="281e4-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="281e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="281e4-102">SYNOPSIS</span></span>
<span data-ttu-id="281e4-103">Wählen Sie ein Abonnement und ein Konto für das Ziel in Azure PowerShell-Cmdlets aus.</span><span class="sxs-lookup"><span data-stu-id="281e4-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="281e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="281e4-104">SYNTAX</span></span>

### <span data-ttu-id="281e4-105">SelectByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="281e4-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="281e4-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="281e4-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="281e4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="281e4-107">DESCRIPTION</span></span>
<span data-ttu-id="281e4-108">Wählen Sie in Azure PowerShell-Cmdlets ein Abonnement für Target (oder Konto oder Mandant) aus.</span><span class="sxs-lookup"><span data-stu-id="281e4-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="281e4-109">Nach diesem Cmdlet werden zukünftige Cmdlets auf den ausgewählten Kontext ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="281e4-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="281e4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="281e4-110">EXAMPLES</span></span>

### <span data-ttu-id="281e4-111">Beispiel 1: Ziel eines benannten Kontexts</span><span class="sxs-lookup"><span data-stu-id="281e4-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="281e4-112">Ziel der zukünftigen Azure PowerShell-Cmdlets für das Konto, den Mandanten und das Abonnement im Kontext "Arbeit".</span><span class="sxs-lookup"><span data-stu-id="281e4-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="281e4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="281e4-113">PARAMETERS</span></span>

### <span data-ttu-id="281e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281e4-114">-DefaultProfile</span></span>
<span data-ttu-id="281e4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="281e4-115">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281e4-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="281e4-116">-InputObject</span></span>
<span data-ttu-id="281e4-117">Ein Kontextobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="281e4-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="281e4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="281e4-118">-Name</span></span>
<span data-ttu-id="281e4-119">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="281e4-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281e4-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="281e4-120">-Scope</span></span>
<span data-ttu-id="281e4-121">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="281e4-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="281e4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="281e4-122">-Confirm</span></span>
<span data-ttu-id="281e4-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="281e4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="281e4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="281e4-124">-WhatIf</span></span>
<span data-ttu-id="281e4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="281e4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="281e4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="281e4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="281e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281e4-127">CommonParameters</span></span>
<span data-ttu-id="281e4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="281e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281e4-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="281e4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281e4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="281e4-130">INPUTS</span></span>

### <span data-ttu-id="281e4-131">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="281e4-131">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="281e4-132">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="281e4-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="281e4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="281e4-133">OUTPUTS</span></span>

### <span data-ttu-id="281e4-134">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="281e4-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="281e4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="281e4-135">NOTES</span></span>

## <span data-ttu-id="281e4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="281e4-136">RELATED LINKS</span></span>
