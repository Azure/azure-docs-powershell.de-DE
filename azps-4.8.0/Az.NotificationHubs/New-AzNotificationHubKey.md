---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174959"
---
# <span data-ttu-id="c316b-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="c316b-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="c316b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c316b-102">SYNOPSIS</span></span>
<span data-ttu-id="c316b-103">Generieren Sie den Autorisierungsregel Schlüssel für eine NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="c316b-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="c316b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c316b-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c316b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c316b-105">DESCRIPTION</span></span>
<span data-ttu-id="c316b-106">New-AzNotificationHubKey-Cmdlet generiert den Primärschlüssel/sekundären Schlüssel für die NotificationHub-Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="c316b-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="c316b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c316b-107">EXAMPLES</span></span>

### <span data-ttu-id="c316b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c316b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c316b-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="c316b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c316b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c316b-110">PARAMETERS</span></span>

### <span data-ttu-id="c316b-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c316b-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="c316b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c316b-112">-DefaultProfile</span></span>
<span data-ttu-id="c316b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c316b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c316b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c316b-114">-Force</span></span>
<span data-ttu-id="c316b-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c316b-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c316b-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c316b-116">-Namespace</span></span>
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

### <span data-ttu-id="c316b-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c316b-117">-NotificationHub</span></span>
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

### <span data-ttu-id="c316b-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c316b-118">-PolicyKey</span></span>
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

### <span data-ttu-id="c316b-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c316b-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="c316b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c316b-120">-Confirm</span></span>
<span data-ttu-id="c316b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c316b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c316b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c316b-122">-WhatIf</span></span>
<span data-ttu-id="c316b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c316b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c316b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c316b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c316b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c316b-125">CommonParameters</span></span>
<span data-ttu-id="c316b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c316b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c316b-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c316b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c316b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c316b-128">INPUTS</span></span>

### <span data-ttu-id="c316b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c316b-129">System.String</span></span>

## <span data-ttu-id="c316b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c316b-130">OUTPUTS</span></span>

### <span data-ttu-id="c316b-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c316b-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c316b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c316b-132">NOTES</span></span>

## <span data-ttu-id="c316b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c316b-133">RELATED LINKS</span></span>
