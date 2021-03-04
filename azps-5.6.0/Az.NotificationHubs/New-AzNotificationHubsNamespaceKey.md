---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 2d3fb02aa41d58521d35382aa35eb47c4b1d523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918195"
---
# <span data-ttu-id="4b9a7-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="4b9a7-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="4b9a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9a7-103">Regenerieren Sie den Autorisierungsregelschlüssel für einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="4b9a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b9a7-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9a7-106">New-AzNotificationHubNamespaceKey cmdlet regeneriert den Primärschlüssel/Sekundärschlüssel für die Namespaceautorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="4b9a7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b9a7-107">EXAMPLES</span></span>

### <span data-ttu-id="4b9a7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b9a7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4b9a7-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="4b9a7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4b9a7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4b9a7-110">PARAMETERS</span></span>

### <span data-ttu-id="4b9a7-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4b9a7-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9a7-112">-DefaultProfile</span></span>
<span data-ttu-id="4b9a7-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4b9a7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b9a7-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="4b9a7-114">-Force</span></span>
<span data-ttu-id="4b9a7-115">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b9a7-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="4b9a7-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b9a7-118">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b9a7-119">-Confirm</span></span>
<span data-ttu-id="4b9a7-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9a7-121">-WhatIf</span></span>
<span data-ttu-id="4b9a7-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b9a7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9a7-124">CommonParameters</span></span>
<span data-ttu-id="4b9a7-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9a7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9a7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9a7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b9a7-127">INPUTS</span></span>

### <span data-ttu-id="4b9a7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b9a7-128">System.String</span></span>

## <span data-ttu-id="4b9a7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b9a7-129">OUTPUTS</span></span>

### <span data-ttu-id="4b9a7-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="4b9a7-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="4b9a7-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4b9a7-131">NOTES</span></span>

## <span data-ttu-id="4b9a7-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4b9a7-132">RELATED LINKS</span></span>
