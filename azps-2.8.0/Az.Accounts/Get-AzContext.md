---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 0f306b7e42dbe5b37c1c814a9458a5e1fb81cc7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658467"
---
# <span data-ttu-id="6bcde-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="6bcde-101">Get-AzContext</span></span>

## <span data-ttu-id="6bcde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6bcde-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcde-103">Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6bcde-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6bcde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bcde-104">SYNTAX</span></span>

### <span data-ttu-id="6bcde-105">Getsinglecontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="6bcde-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="6bcde-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="6bcde-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bcde-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6bcde-107">DESCRIPTION</span></span>
<span data-ttu-id="6bcde-108">Das Get-AzContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6bcde-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="6bcde-109">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="6bcde-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="6bcde-110">Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6bcde-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6bcde-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bcde-111">EXAMPLES</span></span>

### <span data-ttu-id="6bcde-112">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="6bcde-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="6bcde-113">In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Connect-AzAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="6bcde-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="6bcde-114">Beispiel 2: Auflisten aller verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="6bcde-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="6bcde-115">In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6bcde-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="6bcde-116">Der Benutzer kann einen dieser Kontexte mithilfe von SELECT-AzContext auswählen.</span><span class="sxs-lookup"><span data-stu-id="6bcde-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="6bcde-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bcde-117">PARAMETERS</span></span>

### <span data-ttu-id="6bcde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcde-118">-DefaultProfile</span></span>
<span data-ttu-id="6bcde-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6bcde-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bcde-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6bcde-120">-ListAvailable</span></span>
<span data-ttu-id="6bcde-121">Auflisten aller verfügbaren Kontexte in der aktuellen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6bcde-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcde-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6bcde-122">-Name</span></span>
<span data-ttu-id="6bcde-123">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="6bcde-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcde-124">CommonParameters</span></span>
<span data-ttu-id="6bcde-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcde-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcde-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcde-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6bcde-127">INPUTS</span></span>

### <span data-ttu-id="6bcde-128">Keine</span><span class="sxs-lookup"><span data-stu-id="6bcde-128">None</span></span>

## <span data-ttu-id="6bcde-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bcde-129">OUTPUTS</span></span>

### <span data-ttu-id="6bcde-130">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6bcde-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6bcde-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6bcde-131">NOTES</span></span>

## <span data-ttu-id="6bcde-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6bcde-132">RELATED LINKS</span></span>

[<span data-ttu-id="6bcde-133">Satz-AzContext</span><span class="sxs-lookup"><span data-stu-id="6bcde-133">Set-AzContext</span></span>](./Set-AzContext.md)

