---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496530"
---
# <span data-ttu-id="f9486-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="f9486-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="f9486-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9486-102">SYNOPSIS</span></span>
<span data-ttu-id="f9486-103">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="f9486-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9486-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9486-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9486-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9486-105">DESCRIPTION</span></span>
<span data-ttu-id="f9486-106">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="f9486-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="f9486-107">Sie können entweder connectionStrings für alle Schlüssel abrufen oder nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="f9486-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="f9486-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9486-108">EXAMPLES</span></span>

### <span data-ttu-id="f9486-109">Beispiel 1 Abrufen aller IotHub-connectionStrings</span><span class="sxs-lookup"><span data-stu-id="f9486-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f9486-110">Ruft die ConnectionStrings für alle Schlüssel für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="f9486-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="f9486-111">Beispiel 2 Abrufen der IotHub-connectionStrings für einen bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f9486-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="f9486-112">Ruft die ConnectionStrings für den Schlüssel mit dem Namen "MyKey" für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="f9486-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="f9486-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9486-113">PARAMETERS</span></span>

### <span data-ttu-id="f9486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9486-114">-DefaultProfile</span></span>
<span data-ttu-id="f9486-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f9486-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9486-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f9486-116">-KeyName</span></span>
<span data-ttu-id="f9486-117">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="f9486-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9486-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f9486-118">-Name</span></span>
<span data-ttu-id="f9486-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="f9486-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f9486-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9486-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9486-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f9486-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f9486-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9486-122">CommonParameters</span></span>
<span data-ttu-id="f9486-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9486-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9486-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9486-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9486-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9486-125">INPUTS</span></span>

### <span data-ttu-id="f9486-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f9486-126">System.String</span></span>

## <span data-ttu-id="f9486-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9486-127">OUTPUTS</span></span>

### <span data-ttu-id="f9486-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9486-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="f9486-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="f9486-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="f9486-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9486-130">NOTES</span></span>

## <span data-ttu-id="f9486-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9486-131">RELATED LINKS</span></span>

