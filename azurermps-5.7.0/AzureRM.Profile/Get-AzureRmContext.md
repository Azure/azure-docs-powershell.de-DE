---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502537"
---
# <span data-ttu-id="bb1aa-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="bb1aa-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="bb1aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1aa-103">Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb1aa-104">SYNTAX</span></span>

### <span data-ttu-id="bb1aa-105">Getsinglecontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb1aa-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="bb1aa-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="bb1aa-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb1aa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb1aa-107">DESCRIPTION</span></span>
<span data-ttu-id="bb1aa-108">Das Get-AzureRmContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="bb1aa-109">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="bb1aa-110">Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="bb1aa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb1aa-111">EXAMPLES</span></span>

### <span data-ttu-id="bb1aa-112">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="bb1aa-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="bb1aa-113">In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Connect-AzureRmAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="bb1aa-114">Beispiel 2: Auflisten aller verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="bb1aa-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="bb1aa-115">In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="bb1aa-116">Der Benutzer kann einen dieser Kontexte mithilfe von SELECT-AzureRmContext auswählen.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="bb1aa-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb1aa-117">PARAMETERS</span></span>

### <span data-ttu-id="bb1aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1aa-118">-DefaultProfile</span></span>
<span data-ttu-id="bb1aa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb1aa-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1aa-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="bb1aa-120">-ListAvailable</span></span>
<span data-ttu-id="bb1aa-121">Auflisten aller verfügbaren Kontexte in der aktuellen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1aa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb1aa-122">-Name</span></span>
<span data-ttu-id="bb1aa-123">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="bb1aa-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1aa-124">CommonParameters</span></span>
<span data-ttu-id="bb1aa-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1aa-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1aa-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb1aa-127">INPUTS</span></span>

### <span data-ttu-id="bb1aa-128">Keine</span><span class="sxs-lookup"><span data-stu-id="bb1aa-128">None</span></span>
<span data-ttu-id="bb1aa-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb1aa-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb1aa-130">OUTPUTS</span></span>

### <span data-ttu-id="bb1aa-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="bb1aa-131">PSAzureContext</span></span>
<span data-ttu-id="bb1aa-132">Dieses Cmdlet gibt das Konto, den Mandanten und das Abonnement zurück, das von Azure Resource Manager-Cmdlets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb1aa-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="bb1aa-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb1aa-133">NOTES</span></span>

## <span data-ttu-id="bb1aa-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb1aa-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb1aa-135">Satz-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="bb1aa-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

