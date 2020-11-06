---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503697"
---
# <span data-ttu-id="23d68-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="23d68-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="23d68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23d68-102">SYNOPSIS</span></span>
<span data-ttu-id="23d68-103">Generieren Sie den Autorisierungsregel Schlüssel für einen Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="23d68-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d68-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23d68-105">DESCRIPTION</span></span>
<span data-ttu-id="23d68-106">New-AzureRmNotificationHubNamespaceKey-Cmdlet generiert den Primärschlüssel/sekundären Schlüssel für die Namespace Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="23d68-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="23d68-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23d68-107">EXAMPLES</span></span>

### <span data-ttu-id="23d68-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="23d68-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="23d68-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="23d68-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="23d68-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="23d68-110">PARAMETERS</span></span>

### <span data-ttu-id="23d68-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23d68-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d68-112">-DefaultProfile</span></span>
<span data-ttu-id="23d68-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="23d68-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d68-114">-Force</span><span class="sxs-lookup"><span data-stu-id="23d68-114">-Force</span></span>
<span data-ttu-id="23d68-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="23d68-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23d68-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="23d68-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23d68-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23d68-119">-Confirm</span></span>
<span data-ttu-id="23d68-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23d68-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d68-121">-WhatIf</span></span>
<span data-ttu-id="23d68-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23d68-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d68-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23d68-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d68-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d68-124">CommonParameters</span></span>
<span data-ttu-id="23d68-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d68-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d68-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d68-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d68-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23d68-127">INPUTS</span></span>

### <span data-ttu-id="23d68-128">Keine</span><span class="sxs-lookup"><span data-stu-id="23d68-128">None</span></span>
<span data-ttu-id="23d68-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="23d68-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23d68-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23d68-130">OUTPUTS</span></span>

### <span data-ttu-id="23d68-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="23d68-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="23d68-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="23d68-132">NOTES</span></span>

## <span data-ttu-id="23d68-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23d68-133">RELATED LINKS</span></span>

