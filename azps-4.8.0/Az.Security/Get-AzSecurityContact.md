---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165607"
---
# <span data-ttu-id="302d6-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="302d6-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="302d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="302d6-102">SYNOPSIS</span></span>
<span data-ttu-id="302d6-103">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="302d6-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="302d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="302d6-104">SYNTAX</span></span>

### <span data-ttu-id="302d6-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="302d6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="302d6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="302d6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="302d6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="302d6-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="302d6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="302d6-108">DESCRIPTION</span></span>
<span data-ttu-id="302d6-109">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="302d6-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="302d6-110">Der Sicherheitskontakt kann Benachrichtigungen zu Sicherheitswarnungen erhalten, die im Abonnement auftreten.</span><span class="sxs-lookup"><span data-stu-id="302d6-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="302d6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="302d6-111">EXAMPLES</span></span>

### <span data-ttu-id="302d6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="302d6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="302d6-113">Ruft alle konfigurierten Sicherheitskontakte für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="302d6-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="302d6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="302d6-114">PARAMETERS</span></span>

### <span data-ttu-id="302d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302d6-115">-DefaultProfile</span></span>
<span data-ttu-id="302d6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="302d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302d6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="302d6-117">-Name</span></span>
<span data-ttu-id="302d6-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="302d6-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302d6-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="302d6-119">-ResourceId</span></span>
<span data-ttu-id="302d6-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="302d6-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302d6-121">CommonParameters</span></span>
<span data-ttu-id="302d6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302d6-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="302d6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302d6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="302d6-124">INPUTS</span></span>

### <span data-ttu-id="302d6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="302d6-125">System.String</span></span>

## <span data-ttu-id="302d6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="302d6-126">OUTPUTS</span></span>

### <span data-ttu-id="302d6-127">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="302d6-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="302d6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="302d6-128">NOTES</span></span>

## <span data-ttu-id="302d6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="302d6-129">RELATED LINKS</span></span>
