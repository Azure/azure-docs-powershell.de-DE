---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 52c5bee4e699ff063794f140ce4360669180a164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663933"
---
# <span data-ttu-id="1a941-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="1a941-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="1a941-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a941-102">SYNOPSIS</span></span>
<span data-ttu-id="1a941-103">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="1a941-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a941-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a941-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a941-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a941-105">DESCRIPTION</span></span>
<span data-ttu-id="1a941-106">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="1a941-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="1a941-107">Sie können entweder connectionStrings für alle Schlüssel abrufen oder nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="1a941-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="1a941-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a941-108">EXAMPLES</span></span>

### <span data-ttu-id="1a941-109">Beispiel 1 Abrufen aller IotHub-connectionStrings</span><span class="sxs-lookup"><span data-stu-id="1a941-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1a941-110">Ruft die ConnectionStrings für alle Schlüssel für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="1a941-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="1a941-111">Beispiel 2 Abrufen der IotHub-connectionStrings für einen bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1a941-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="1a941-112">Ruft die ConnectionStrings für den Schlüssel mit dem Namen "MyKey" für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="1a941-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="1a941-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a941-113">PARAMETERS</span></span>

### <span data-ttu-id="1a941-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1a941-114">-KeyName</span></span>
<span data-ttu-id="1a941-115">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="1a941-115">Name of the Key</span></span>

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

### <span data-ttu-id="1a941-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1a941-116">-Name</span></span>
<span data-ttu-id="1a941-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="1a941-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="1a941-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a941-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a941-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1a941-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1a941-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a941-120">-DefaultProfile</span></span>
<span data-ttu-id="1a941-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a941-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a941-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a941-122">CommonParameters</span></span>
<span data-ttu-id="1a941-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a941-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a941-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a941-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a941-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a941-125">INPUTS</span></span>

### <span data-ttu-id="1a941-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1a941-126">System.String</span></span>

## <span data-ttu-id="1a941-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a941-127">OUTPUTS</span></span>

### <span data-ttu-id="1a941-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1a941-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="1a941-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="1a941-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="1a941-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a941-130">NOTES</span></span>

## <span data-ttu-id="1a941-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a941-131">RELATED LINKS</span></span>

