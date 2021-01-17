---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98461000"
---
# <span data-ttu-id="60f8d-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="60f8d-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="60f8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="60f8d-103">Erstellen Sie den Autorisierungsregelschlüssel für einen NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="60f8d-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="60f8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60f8d-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f8d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60f8d-105">DESCRIPTION</span></span>
<span data-ttu-id="60f8d-106">New-AzNotificationHubKey cmdlet generiert den Primärschlüssel/Sekundärschlüssel für die NotificationHub-Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="60f8d-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="60f8d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60f8d-107">EXAMPLES</span></span>

### <span data-ttu-id="60f8d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60f8d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="60f8d-109">{{ Beispielbeschreibung hier hinzufügen }}</span><span class="sxs-lookup"><span data-stu-id="60f8d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="60f8d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60f8d-110">PARAMETERS</span></span>

### <span data-ttu-id="60f8d-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60f8d-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="60f8d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f8d-112">-DefaultProfile</span></span>
<span data-ttu-id="60f8d-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="60f8d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f8d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="60f8d-114">-Force</span></span>
<span data-ttu-id="60f8d-115">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="60f8d-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60f8d-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="60f8d-116">-Namespace</span></span>
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

### <span data-ttu-id="60f8d-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="60f8d-117">-NotificationHub</span></span>
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

### <span data-ttu-id="60f8d-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="60f8d-118">-PolicyKey</span></span>
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

### <span data-ttu-id="60f8d-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60f8d-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="60f8d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60f8d-120">-Confirm</span></span>
<span data-ttu-id="60f8d-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60f8d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f8d-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="60f8d-122">-WhatIf</span></span>
<span data-ttu-id="60f8d-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60f8d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f8d-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60f8d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f8d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f8d-125">CommonParameters</span></span>
<span data-ttu-id="60f8d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f8d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f8d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f8d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f8d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60f8d-128">INPUTS</span></span>

### <span data-ttu-id="60f8d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="60f8d-129">System.String</span></span>

## <span data-ttu-id="60f8d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60f8d-130">OUTPUTS</span></span>

### <span data-ttu-id="60f8d-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="60f8d-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="60f8d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60f8d-132">NOTES</span></span>

## <span data-ttu-id="60f8d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60f8d-133">RELATED LINKS</span></span>
