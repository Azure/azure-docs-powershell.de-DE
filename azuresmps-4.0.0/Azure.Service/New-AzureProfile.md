---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006206"
---
# <span data-ttu-id="e423e-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="e423e-101">New-AzureProfile</span></span>

## <span data-ttu-id="e423e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e423e-102">SYNOPSIS</span></span>

## <span data-ttu-id="e423e-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="e423e-103">SYNTAX</span></span>

### <span data-ttu-id="e423e-104">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="e423e-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="e423e-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e423e-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="e423e-106">Token</span><span class="sxs-lookup"><span data-stu-id="e423e-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="e423e-107">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e423e-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="e423e-108">Leer</span><span class="sxs-lookup"><span data-stu-id="e423e-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="e423e-109">Datei</span><span class="sxs-lookup"><span data-stu-id="e423e-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="e423e-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="e423e-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="e423e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e423e-111">DESCRIPTION</span></span>

## <span data-ttu-id="e423e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e423e-112">EXAMPLES</span></span>

### <span data-ttu-id="e423e-113">1:</span><span class="sxs-lookup"><span data-stu-id="e423e-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e423e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e423e-114">PARAMETERS</span></span>

### <span data-ttu-id="e423e-115">-Access Token</span><span class="sxs-lookup"><span data-stu-id="e423e-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-116">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="e423e-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-117">-Zertifikat</span><span class="sxs-lookup"><span data-stu-id="e423e-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e423e-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-119">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="e423e-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-120">-Path</span><span class="sxs-lookup"><span data-stu-id="e423e-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-121">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e423e-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e423e-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e423e-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e423e-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-125">-Mandant</span><span class="sxs-lookup"><span data-stu-id="e423e-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e423e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e423e-126">CommonParameters</span></span>
<span data-ttu-id="e423e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e423e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e423e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e423e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e423e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e423e-129">INPUTS</span></span>

## <span data-ttu-id="e423e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e423e-130">OUTPUTS</span></span>

## <span data-ttu-id="e423e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e423e-131">NOTES</span></span>

## <span data-ttu-id="e423e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e423e-132">RELATED LINKS</span></span>

