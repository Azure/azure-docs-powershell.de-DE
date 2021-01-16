---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289822"
---
# <span data-ttu-id="5cd34-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="5cd34-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="5cd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd34-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd34-103">Ruft Sicherheitskontakte ab, die in diesem Abonnement konfiguriert wurden</span><span class="sxs-lookup"><span data-stu-id="5cd34-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="5cd34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cd34-104">SYNTAX</span></span>

### <span data-ttu-id="5cd34-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cd34-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd34-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5cd34-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cd34-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd34-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cd34-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cd34-108">DESCRIPTION</span></span>
<span data-ttu-id="5cd34-109">Ruft Sicherheitskontakte ab, die in diesem Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="5cd34-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="5cd34-110">Der Sicherheitskontakt kann Benachrichtigungen zu Sicherheitswarnungen erhalten, die im Abonnement auftreten.</span><span class="sxs-lookup"><span data-stu-id="5cd34-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="5cd34-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cd34-111">EXAMPLES</span></span>

### <span data-ttu-id="5cd34-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cd34-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="5cd34-113">Ruft alle konfigurierten Sicherheitskontakte im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5cd34-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="5cd34-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd34-114">PARAMETERS</span></span>

### <span data-ttu-id="5cd34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd34-115">-DefaultProfile</span></span>
<span data-ttu-id="5cd34-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cd34-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd34-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd34-117">-Name</span></span>
<span data-ttu-id="5cd34-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5cd34-118">Resource name.</span></span>

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

### <span data-ttu-id="5cd34-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd34-119">-ResourceId</span></span>
<span data-ttu-id="5cd34-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5cd34-120">Resource ID.</span></span>

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

### <span data-ttu-id="5cd34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd34-121">CommonParameters</span></span>
<span data-ttu-id="5cd34-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd34-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cd34-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd34-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cd34-124">INPUTS</span></span>

### <span data-ttu-id="5cd34-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd34-125">System.String</span></span>

## <span data-ttu-id="5cd34-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cd34-126">OUTPUTS</span></span>

### <span data-ttu-id="5cd34-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="5cd34-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="5cd34-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cd34-128">NOTES</span></span>

## <span data-ttu-id="5cd34-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cd34-129">RELATED LINKS</span></span>
