---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009249"
---
# <span data-ttu-id="bef29-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="bef29-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="bef29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bef29-102">SYNOPSIS</span></span>
<span data-ttu-id="bef29-103">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="bef29-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="bef29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bef29-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bef29-105">DESCRIPTION</span></span>
<span data-ttu-id="bef29-106">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="bef29-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="bef29-107">Sie können entweder connectionStrings für alle Schlüssel abrufen oder nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="bef29-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="bef29-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bef29-108">EXAMPLES</span></span>

### <span data-ttu-id="bef29-109">Beispiel 1 Abrufen aller IotHub-connectionStrings</span><span class="sxs-lookup"><span data-stu-id="bef29-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bef29-110">Ruft die ConnectionStrings für alle Schlüssel für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="bef29-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="bef29-111">Beispiel 2 Abrufen der IotHub-connectionStrings für einen bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="bef29-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="bef29-112">Ruft die ConnectionStrings für den Schlüssel mit dem Namen "MyKey" für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="bef29-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="bef29-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bef29-113">PARAMETERS</span></span>

### <span data-ttu-id="bef29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef29-114">-DefaultProfile</span></span>
<span data-ttu-id="bef29-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bef29-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bef29-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bef29-116">-KeyName</span></span>
<span data-ttu-id="bef29-117">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bef29-117">Name of the Key</span></span>

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

### <span data-ttu-id="bef29-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bef29-118">-Name</span></span>
<span data-ttu-id="bef29-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="bef29-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="bef29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef29-120">-ResourceGroupName</span></span>
<span data-ttu-id="bef29-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bef29-121">Resource Group Name</span></span>

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

### <span data-ttu-id="bef29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef29-122">CommonParameters</span></span>
<span data-ttu-id="bef29-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef29-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef29-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef29-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bef29-125">INPUTS</span></span>

### <span data-ttu-id="bef29-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bef29-126">System.String</span></span>

## <span data-ttu-id="bef29-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bef29-127">OUTPUTS</span></span>

### <span data-ttu-id="bef29-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bef29-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="bef29-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="bef29-129">NOTES</span></span>

## <span data-ttu-id="bef29-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bef29-130">RELATED LINKS</span></span>
