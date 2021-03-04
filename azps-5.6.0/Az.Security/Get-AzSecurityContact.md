---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: a00edef30c327e9bce4e2fa008dad373a2e6367d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932283"
---
# <span data-ttu-id="3245f-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3245f-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="3245f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3245f-102">SYNOPSIS</span></span>
<span data-ttu-id="3245f-103">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden</span><span class="sxs-lookup"><span data-stu-id="3245f-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="3245f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3245f-104">SYNTAX</span></span>

### <span data-ttu-id="3245f-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="3245f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3245f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3245f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3245f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3245f-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3245f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3245f-108">DESCRIPTION</span></span>
<span data-ttu-id="3245f-109">Ruft Sicherheitskontakte ab, die für dieses Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="3245f-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="3245f-110">Der Sicherheitskontakt kann Benachrichtigungen zu Sicherheitsbenachrichtigungen erhalten, die im Abonnement auftreten.</span><span class="sxs-lookup"><span data-stu-id="3245f-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="3245f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3245f-111">EXAMPLES</span></span>

### <span data-ttu-id="3245f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3245f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="3245f-113">Ruft alle konfigurierten Sicherheitskontakte im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3245f-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="3245f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3245f-114">PARAMETERS</span></span>

### <span data-ttu-id="3245f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3245f-115">-DefaultProfile</span></span>
<span data-ttu-id="3245f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3245f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3245f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3245f-117">-Name</span></span>
<span data-ttu-id="3245f-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3245f-118">Resource name.</span></span>

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

### <span data-ttu-id="3245f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3245f-119">-ResourceId</span></span>
<span data-ttu-id="3245f-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3245f-120">Resource ID.</span></span>

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

### <span data-ttu-id="3245f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3245f-121">CommonParameters</span></span>
<span data-ttu-id="3245f-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3245f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3245f-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3245f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3245f-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3245f-124">INPUTS</span></span>

### <span data-ttu-id="3245f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3245f-125">System.String</span></span>

## <span data-ttu-id="3245f-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3245f-126">OUTPUTS</span></span>

### <span data-ttu-id="3245f-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="3245f-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="3245f-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3245f-128">NOTES</span></span>

## <span data-ttu-id="3245f-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3245f-129">RELATED LINKS</span></span>
