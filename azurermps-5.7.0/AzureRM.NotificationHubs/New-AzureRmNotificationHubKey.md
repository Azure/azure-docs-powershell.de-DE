---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 66d947cc9d5765fdbfeb815019bbd739f7c3d819
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504505"
---
# <span data-ttu-id="9b1d1-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="9b1d1-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="9b1d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1d1-103">Generieren Sie den Autorisierungsregel Schlüssel für eine NotificationHub erneut.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b1d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b1d1-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="9b1d1-106">New-AzureRmNotificationHubKey-Cmdlet generiert den Primärschlüssel/sekundären Schlüssel für die NotificationHub-Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="9b1d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b1d1-107">EXAMPLES</span></span>

### <span data-ttu-id="9b1d1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b1d1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9b1d1-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="9b1d1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9b1d1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="9b1d1-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b1d1-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d1-112">-DefaultProfile</span></span>
<span data-ttu-id="9b1d1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9b1d1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b1d1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9b1d1-114">-Force</span></span>
<span data-ttu-id="9b1d1-115">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b1d1-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b1d1-116">-Namespace</span></span>
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

### <span data-ttu-id="9b1d1-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9b1d1-117">-NotificationHub</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1d1-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="9b1d1-118">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1d1-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b1d1-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="9b1d1-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b1d1-120">-Confirm</span></span>
<span data-ttu-id="9b1d1-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b1d1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1d1-122">-WhatIf</span></span>
<span data-ttu-id="9b1d1-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b1d1-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b1d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1d1-125">CommonParameters</span></span>
<span data-ttu-id="9b1d1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1d1-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b1d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1d1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b1d1-128">INPUTS</span></span>

### <span data-ttu-id="9b1d1-129">Keine</span><span class="sxs-lookup"><span data-stu-id="9b1d1-129">None</span></span>
<span data-ttu-id="9b1d1-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9b1d1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b1d1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b1d1-131">OUTPUTS</span></span>

### <span data-ttu-id="9b1d1-132">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9b1d1-132">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="9b1d1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b1d1-133">NOTES</span></span>

## <span data-ttu-id="9b1d1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b1d1-134">RELATED LINKS</span></span>

