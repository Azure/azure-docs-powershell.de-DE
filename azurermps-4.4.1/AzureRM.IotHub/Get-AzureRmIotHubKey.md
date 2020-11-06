---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501829"
---
# <span data-ttu-id="563f3-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="563f3-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="563f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="563f3-102">SYNOPSIS</span></span>
<span data-ttu-id="563f3-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="563f3-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="563f3-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="563f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="563f3-105">DESCRIPTION</span></span>
<span data-ttu-id="563f3-106">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="563f3-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="563f3-107">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="563f3-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="563f3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="563f3-108">EXAMPLES</span></span>

### <span data-ttu-id="563f3-109">Beispiel 1 Abrufen aller Schlüssel</span><span class="sxs-lookup"><span data-stu-id="563f3-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="563f3-110">Ruft alle Schlüssel für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="563f3-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="563f3-111">Beispiel 2 Abrufen von Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="563f3-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="563f3-112">Ruft die Informationen für einen Schlüssel mit dem Namen "iothubowner" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="563f3-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="563f3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="563f3-113">PARAMETERS</span></span>

### <span data-ttu-id="563f3-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="563f3-114">-KeyName</span></span>
<span data-ttu-id="563f3-115">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="563f3-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563f3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="563f3-116">-Name</span></span>
<span data-ttu-id="563f3-117">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="563f3-117">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="563f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="563f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="563f3-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="563f3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="563f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563f3-120">-DefaultProfile</span></span>
<span data-ttu-id="563f3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="563f3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="563f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563f3-122">CommonParameters</span></span>
<span data-ttu-id="563f3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="563f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563f3-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563f3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563f3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="563f3-125">INPUTS</span></span>

### <span data-ttu-id="563f3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="563f3-126">System.String</span></span>

## <span data-ttu-id="563f3-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="563f3-127">OUTPUTS</span></span>

### <span data-ttu-id="563f3-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="563f3-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="563f3-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="563f3-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="563f3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="563f3-130">NOTES</span></span>

## <span data-ttu-id="563f3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="563f3-131">RELATED LINKS</span></span>

