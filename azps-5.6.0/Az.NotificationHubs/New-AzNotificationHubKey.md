---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 8c6b24dd2d208ea4465138f1e901b030ee5c30e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918248"
---
# <span data-ttu-id="9f074-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="9f074-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="9f074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f074-102">SYNOPSIS</span></span>
<span data-ttu-id="9f074-103">Regenerieren Sie den Autorisierungsregelschlüssel für einen NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="9f074-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="9f074-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f074-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f074-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f074-105">DESCRIPTION</span></span>
<span data-ttu-id="9f074-106">New-AzNotificationHubKey cmdlet regeneriert den Primärschlüssel/Sekundärschlüssel für die NotificationHub-Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="9f074-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="9f074-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f074-107">EXAMPLES</span></span>

### <span data-ttu-id="9f074-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9f074-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9f074-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="9f074-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9f074-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f074-110">PARAMETERS</span></span>

### <span data-ttu-id="9f074-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9f074-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f074-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f074-112">-DefaultProfile</span></span>
<span data-ttu-id="9f074-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9f074-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f074-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="9f074-114">-Force</span></span>
<span data-ttu-id="9f074-115">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="9f074-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9f074-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f074-116">-Namespace</span></span>
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

### <span data-ttu-id="9f074-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9f074-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f074-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="9f074-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f074-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f074-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="9f074-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f074-120">-Confirm</span></span>
<span data-ttu-id="9f074-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f074-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f074-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f074-122">-WhatIf</span></span>
<span data-ttu-id="9f074-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f074-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f074-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f074-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f074-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f074-125">CommonParameters</span></span>
<span data-ttu-id="9f074-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f074-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f074-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f074-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f074-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f074-128">INPUTS</span></span>

### <span data-ttu-id="9f074-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9f074-129">System.String</span></span>

## <span data-ttu-id="9f074-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f074-130">OUTPUTS</span></span>

### <span data-ttu-id="9f074-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9f074-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="9f074-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f074-132">NOTES</span></span>

## <span data-ttu-id="9f074-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f074-133">RELATED LINKS</span></span>
