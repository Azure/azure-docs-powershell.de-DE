---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664004"
---
# <span data-ttu-id="c4d17-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c4d17-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="c4d17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4d17-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d17-103">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4d17-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4d17-104">SYNTAX</span></span>

### <span data-ttu-id="c4d17-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4d17-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d17-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c4d17-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d17-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d17-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4d17-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4d17-108">DESCRIPTION</span></span>
<span data-ttu-id="c4d17-109">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4d17-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="c4d17-110">Der Sicherheitskontakt kann Benachrichtigungen zu Sicherheitswarnungen erhalten, die im Abonnement auftreten.</span><span class="sxs-lookup"><span data-stu-id="c4d17-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="c4d17-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4d17-111">EXAMPLES</span></span>

### <span data-ttu-id="c4d17-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4d17-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="c4d17-113">Ruft alle konfigurierten Sicherheitskontakte für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c4d17-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="c4d17-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4d17-114">PARAMETERS</span></span>

### <span data-ttu-id="c4d17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d17-115">-DefaultProfile</span></span>
<span data-ttu-id="c4d17-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4d17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d17-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c4d17-117">-Name</span></span>
<span data-ttu-id="c4d17-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c4d17-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d17-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c4d17-119">-ResourceId</span></span>
<span data-ttu-id="c4d17-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c4d17-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d17-121">CommonParameters</span></span>
<span data-ttu-id="c4d17-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d17-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d17-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d17-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4d17-124">INPUTS</span></span>

### <span data-ttu-id="c4d17-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d17-125">System.String</span></span>

## <span data-ttu-id="c4d17-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4d17-126">OUTPUTS</span></span>

### <span data-ttu-id="c4d17-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c4d17-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="c4d17-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4d17-128">NOTES</span></span>

## <span data-ttu-id="c4d17-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4d17-129">RELATED LINKS</span></span>
