---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145356"
---
# <span data-ttu-id="080c2-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="080c2-101">Get-AzContext</span></span>

## <span data-ttu-id="080c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="080c2-102">SYNOPSIS</span></span>
<span data-ttu-id="080c2-103">Ruft die Metadaten ab, die zum Authentifizieren von Azure Resource Manager-Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="080c2-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="080c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="080c2-104">SYNTAX</span></span>

### <span data-ttu-id="080c2-105">GetSingleContext (Standard)</span><span class="sxs-lookup"><span data-stu-id="080c2-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="080c2-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="080c2-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="080c2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="080c2-107">DESCRIPTION</span></span>
<span data-ttu-id="080c2-108">Das Get-AzContext ruft die aktuellen Metadaten ab, die zum Authentifizieren von Azure Resource Manager-Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="080c2-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="080c2-109">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die gezielte Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="080c2-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="080c2-110">Azure Resource -Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure Resource Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="080c2-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="080c2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="080c2-111">EXAMPLES</span></span>

### <span data-ttu-id="080c2-112">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="080c2-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="080c2-113">In diesem Beispiel werden wir uns mit einem Azure-Abonnement über Connect-AzAccount bei unserem Konto anmelden und dann den Kontext der aktuellen Sitzung abrufen, indem wir Get-AzContext aufrufen.</span><span class="sxs-lookup"><span data-stu-id="080c2-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="080c2-114">Beispiel 2: Auflisten aller verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="080c2-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="080c2-115">In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="080c2-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="080c2-116">Der Benutzer kann mithilfe von Select-AzContext einen dieser Kontexte auswählen.</span><span class="sxs-lookup"><span data-stu-id="080c2-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="080c2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="080c2-117">PARAMETERS</span></span>

### <span data-ttu-id="080c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080c2-118">-DefaultProfile</span></span>
<span data-ttu-id="080c2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="080c2-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="080c2-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="080c2-120">-ListAvailable</span></span>
<span data-ttu-id="080c2-121">Listet alle verfügbaren Kontexte in der aktuellen Sitzung auf.</span><span class="sxs-lookup"><span data-stu-id="080c2-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="080c2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="080c2-122">-Name</span></span>
<span data-ttu-id="080c2-123">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="080c2-123">The name of the context</span></span>

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

### <span data-ttu-id="080c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080c2-124">CommonParameters</span></span>
<span data-ttu-id="080c2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="080c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080c2-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="080c2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080c2-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="080c2-127">INPUTS</span></span>

### <span data-ttu-id="080c2-128">Keine</span><span class="sxs-lookup"><span data-stu-id="080c2-128">None</span></span>

## <span data-ttu-id="080c2-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="080c2-129">OUTPUTS</span></span>

### <span data-ttu-id="080c2-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="080c2-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="080c2-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="080c2-131">NOTES</span></span>

## <span data-ttu-id="080c2-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="080c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="080c2-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="080c2-133">Set-AzContext</span></span>](./Set-AzContext.md)

