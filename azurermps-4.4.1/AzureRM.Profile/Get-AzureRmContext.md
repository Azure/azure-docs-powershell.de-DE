---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 3ad029e84245aee45bbcdd08ea0d78c5e57b985e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496966"
---
# <span data-ttu-id="f78e7-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f78e7-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="f78e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f78e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f78e7-103">Ruft die Metadaten ab, mit denen Azure Resource Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f78e7-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f78e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f78e7-104">SYNTAX</span></span>

### <span data-ttu-id="f78e7-105">Getsinglecontext (Standard)</span><span class="sxs-lookup"><span data-stu-id="f78e7-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="f78e7-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="f78e7-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f78e7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f78e7-107">DESCRIPTION</span></span>
<span data-ttu-id="f78e7-108">Das Get-AzureRmContext-Cmdlet ruft die aktuellen Metadaten ab, mit denen Azure-Ressourcen-Manager-Anforderungen authentifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f78e7-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="f78e7-109">Dieses Cmdlet ruft das Active Directory-Konto, den Active Directory-Mandanten, das Azure-Abonnement und die Ziel Azure-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="f78e7-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="f78e7-110">Azure Resource Manager-Cmdlets verwenden diese Einstellungen standardmäßig beim Erstellen von Azure-Ressourcen-Manager-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="f78e7-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f78e7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f78e7-111">EXAMPLES</span></span>

### <span data-ttu-id="f78e7-112">Beispiel 1: Abrufen des aktuellen Kontexts</span><span class="sxs-lookup"><span data-stu-id="f78e7-112">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f78e7-113">In diesem Beispiel melden wir uns mit einem Azure-Abonnement mit Add-AzureRmAccount bei unserem Konto an, und dann erhalten wir den Kontext der aktuellen Sitzung durch Aufrufen von Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="f78e7-113">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="f78e7-114">Beispiel 2: Auflisten aller verfügbaren Kontexte</span><span class="sxs-lookup"><span data-stu-id="f78e7-114">Example 2: Listing all available contexts</span></span>
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

<span data-ttu-id="f78e7-115">In diesem Beispiel werden alle derzeit verfügbaren Kontexte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f78e7-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="f78e7-116">Der Benutzer kann einen dieser Kontexte mithilfe von SELECT-AzureRmContext auswählen.</span><span class="sxs-lookup"><span data-stu-id="f78e7-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="f78e7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f78e7-117">PARAMETERS</span></span>

### <span data-ttu-id="f78e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78e7-118">-DefaultProfile</span></span>
<span data-ttu-id="f78e7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f78e7-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f78e7-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f78e7-120">-ListAvailable</span></span>
<span data-ttu-id="f78e7-121">Auflisten aller verfügbaren Kontexte in der aktuellen Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f78e7-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="f78e7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f78e7-122">-Name</span></span>
<span data-ttu-id="f78e7-123">Der Name des Kontexts</span><span class="sxs-lookup"><span data-stu-id="f78e7-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78e7-124">CommonParameters</span></span>
<span data-ttu-id="f78e7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78e7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f78e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78e7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f78e7-127">INPUTS</span></span>

## <span data-ttu-id="f78e7-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f78e7-128">OUTPUTS</span></span>

### <span data-ttu-id="f78e7-129">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f78e7-129">PSAzureContext</span></span>
<span data-ttu-id="f78e7-130">Dieses Cmdlet gibt das Konto, den Mandanten und das Abonnement zurück, das von Azure Resource Manager-Cmdlets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f78e7-130">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="f78e7-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f78e7-131">NOTES</span></span>

## <span data-ttu-id="f78e7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f78e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="f78e7-133">Satz-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f78e7-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

