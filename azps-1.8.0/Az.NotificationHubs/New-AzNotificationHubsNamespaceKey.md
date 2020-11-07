---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 01ba4388d1cb6166c927096144e628d9fc2d81a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660094"
---
# <span data-ttu-id="c4042-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="c4042-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="c4042-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4042-102">SYNOPSIS</span></span>
<span data-ttu-id="c4042-103">Generieren Sie den Autorisierungsregel Schlüssel für einen Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="c4042-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="c4042-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4042-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4042-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4042-105">DESCRIPTION</span></span>
<span data-ttu-id="c4042-106">New-AzNotificationHubNamespaceKey-Cmdlet generiert den Primärschlüssel/sekundären Schlüssel für die Namespace Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="c4042-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="c4042-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4042-107">EXAMPLES</span></span>

### <span data-ttu-id="c4042-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4042-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c4042-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="c4042-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c4042-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4042-110">PARAMETERS</span></span>

### <span data-ttu-id="c4042-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4042-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="c4042-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4042-112">-DefaultProfile</span></span>
<span data-ttu-id="c4042-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c4042-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4042-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c4042-114">-Force</span></span>
<span data-ttu-id="c4042-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c4042-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4042-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4042-116">-Namespace</span></span>
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

### <span data-ttu-id="c4042-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c4042-117">-PolicyKey</span></span>
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

### <span data-ttu-id="c4042-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c4042-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="c4042-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4042-119">-Confirm</span></span>
<span data-ttu-id="c4042-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4042-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4042-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4042-121">-WhatIf</span></span>
<span data-ttu-id="c4042-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4042-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4042-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4042-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4042-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4042-124">CommonParameters</span></span>
<span data-ttu-id="c4042-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4042-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4042-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4042-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4042-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4042-127">INPUTS</span></span>

### <span data-ttu-id="c4042-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c4042-128">System.String</span></span>

## <span data-ttu-id="c4042-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4042-129">OUTPUTS</span></span>

### <span data-ttu-id="c4042-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c4042-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c4042-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4042-131">NOTES</span></span>

## <span data-ttu-id="c4042-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4042-132">RELATED LINKS</span></span>
