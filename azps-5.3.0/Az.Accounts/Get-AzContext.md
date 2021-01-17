---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471589"
---
# <span data-ttu-id="ccba7-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="ccba7-101">Get-AzContext</span></span>

## <span data-ttu-id="ccba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccba7-102">SYNOPSIS</span></span>
<span data-ttu-id="ccba7-103">Ruft die Metadaten ab, die zum Authentifizieren von Azure Resource Manager-Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccba7-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ccba7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccba7-104">SYNTAX</span></span>

### <span data-ttu-id="ccba7-105">GetSingleContext (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccba7-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccba7-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="ccba7-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccba7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccba7-107">DESCRIPTION</span></span>
<span data-ttu-id="ccba7-108">Das Get-AzContext ruft die aktuellen Metadaten ab, die zum Authentifizieren von Azure Resource Manager-Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccba7-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="ccba7-109">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die gezielte Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="ccba7-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="ccba7-110">Azure Resource -Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure Resource Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="ccba7-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="ccba7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ccba7-111">EXAMPLES</span></span>

### <span data-ttu-id="ccba7-112">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="ccba7-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ccba7-113">In diesem Beispiel werden wir uns mit einem Azure-Abonnement über Connect-AzAccount bei unserem Konto anmelden und dann den Kontext der aktuellen Sitzung abrufen, indem wir Get-AzContext aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ccba7-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="ccba7-114">Beispiel 2: Auflisten aller verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="ccba7-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ccba7-115">In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ccba7-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="ccba7-116">Der Benutzer kann mithilfe von Select-AzContext einen dieser Kontexte auswählen.</span><span class="sxs-lookup"><span data-stu-id="ccba7-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="ccba7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccba7-117">PARAMETERS</span></span>

### <span data-ttu-id="ccba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccba7-118">-DefaultProfile</span></span>
<span data-ttu-id="ccba7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ccba7-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccba7-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="ccba7-120">-ListAvailable</span></span>
<span data-ttu-id="ccba7-121">Listet alle verfügbaren Kontexte in der aktuellen Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="ccba7-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="ccba7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ccba7-122">-Name</span></span>
<span data-ttu-id="ccba7-123">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="ccba7-123">The name of the context</span></span>

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

### <span data-ttu-id="ccba7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccba7-124">CommonParameters</span></span>
<span data-ttu-id="ccba7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccba7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccba7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccba7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccba7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ccba7-127">INPUTS</span></span>

### <span data-ttu-id="ccba7-128">Keine</span><span class="sxs-lookup"><span data-stu-id="ccba7-128">None</span></span>

## <span data-ttu-id="ccba7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ccba7-129">OUTPUTS</span></span>

### <span data-ttu-id="ccba7-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ccba7-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ccba7-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ccba7-131">NOTES</span></span>

## <span data-ttu-id="ccba7-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ccba7-132">RELATED LINKS</span></span>

[<span data-ttu-id="ccba7-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="ccba7-133">Set-AzContext</span></span>](./Set-AzContext.md)

