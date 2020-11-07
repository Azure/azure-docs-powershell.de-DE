---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662426"
---
# <span data-ttu-id="fb365-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="fb365-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="fb365-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb365-102">SYNOPSIS</span></span>
<span data-ttu-id="fb365-103">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="fb365-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb365-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb365-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb365-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb365-105">DESCRIPTION</span></span>
<span data-ttu-id="fb365-106">Entfernt einen IotHub-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="fb365-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="fb365-107">Wenn mehrere Schlüssel mit demselben Namen vorhanden sind, wird der erste in der Liste entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb365-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="fb365-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb365-108">EXAMPLES</span></span>

### <span data-ttu-id="fb365-109">Beispiel 1 Löschen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="fb365-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="fb365-110">Entfernt den Schlüssel mit dem Namen iothubowner1 aus dem IotHub mit dem Namen "myiothub".</span><span class="sxs-lookup"><span data-stu-id="fb365-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fb365-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb365-111">PARAMETERS</span></span>

### <span data-ttu-id="fb365-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fb365-112">-KeyName</span></span>
<span data-ttu-id="fb365-113">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="fb365-113">Name of the Key</span></span>

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

### <span data-ttu-id="fb365-114">-Name</span><span class="sxs-lookup"><span data-stu-id="fb365-114">-Name</span></span>
<span data-ttu-id="fb365-115">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="fb365-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="fb365-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb365-116">-ResourceGroupName</span></span>
<span data-ttu-id="fb365-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fb365-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fb365-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb365-118">-Confirm</span></span>
<span data-ttu-id="fb365-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb365-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb365-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb365-120">-WhatIf</span></span>
<span data-ttu-id="fb365-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb365-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb365-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb365-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb365-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb365-123">-DefaultProfile</span></span>
<span data-ttu-id="fb365-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb365-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb365-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb365-125">CommonParameters</span></span>
<span data-ttu-id="fb365-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb365-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb365-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb365-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb365-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb365-128">INPUTS</span></span>

### <span data-ttu-id="fb365-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fb365-129">System.String</span></span>

## <span data-ttu-id="fb365-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb365-130">OUTPUTS</span></span>

### <span data-ttu-id="fb365-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fb365-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fb365-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb365-132">NOTES</span></span>

## <span data-ttu-id="fb365-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb365-133">RELATED LINKS</span></span>

