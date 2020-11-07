---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: f426dc06d08e10d0811382b00e2072f65ebf1b0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660108"
---
# <span data-ttu-id="24793-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="24793-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="24793-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24793-102">SYNOPSIS</span></span>
<span data-ttu-id="24793-103">Generieren Sie den Autorisierungsregel Schlüssel für eine NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="24793-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="24793-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24793-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24793-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24793-105">DESCRIPTION</span></span>
<span data-ttu-id="24793-106">New-AzNotificationHubKey-Cmdlet generiert den Primärschlüssel/sekundären Schlüssel für die NotificationHub-Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="24793-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="24793-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24793-107">EXAMPLES</span></span>

### <span data-ttu-id="24793-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24793-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="24793-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="24793-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="24793-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24793-110">PARAMETERS</span></span>

### <span data-ttu-id="24793-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24793-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="24793-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24793-112">-DefaultProfile</span></span>
<span data-ttu-id="24793-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="24793-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24793-114">-Force</span><span class="sxs-lookup"><span data-stu-id="24793-114">-Force</span></span>
<span data-ttu-id="24793-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="24793-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24793-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24793-116">-Namespace</span></span>
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

### <span data-ttu-id="24793-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="24793-117">-NotificationHub</span></span>
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

### <span data-ttu-id="24793-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="24793-118">-PolicyKey</span></span>
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

### <span data-ttu-id="24793-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24793-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="24793-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24793-120">-Confirm</span></span>
<span data-ttu-id="24793-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24793-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24793-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24793-122">-WhatIf</span></span>
<span data-ttu-id="24793-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24793-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24793-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24793-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24793-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24793-125">CommonParameters</span></span>
<span data-ttu-id="24793-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24793-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24793-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24793-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24793-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24793-128">INPUTS</span></span>

### <span data-ttu-id="24793-129">System. String</span><span class="sxs-lookup"><span data-stu-id="24793-129">System.String</span></span>

## <span data-ttu-id="24793-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24793-130">OUTPUTS</span></span>

### <span data-ttu-id="24793-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="24793-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="24793-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="24793-132">NOTES</span></span>

## <span data-ttu-id="24793-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24793-133">RELATED LINKS</span></span>
