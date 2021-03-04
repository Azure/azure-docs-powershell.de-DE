---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936939"
---
# <span data-ttu-id="30f29-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="30f29-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="30f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f29-102">SYNOPSIS</span></span>
<span data-ttu-id="30f29-103">Ruft die IotHub-Verbindungszeichenfolgen ab.</span><span class="sxs-lookup"><span data-stu-id="30f29-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="30f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30f29-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30f29-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30f29-105">DESCRIPTION</span></span>
<span data-ttu-id="30f29-106">Ruft die IotHub-Verbindungszeichenfolgen ab.</span><span class="sxs-lookup"><span data-stu-id="30f29-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="30f29-107">Sie können entweder Verbindungszeichenfolgen für alle Schlüssel erhalten oder sie nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="30f29-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="30f29-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30f29-108">EXAMPLES</span></span>

### <span data-ttu-id="30f29-109">Beispiel 1 Alle IotHub-Verbindungszeichenfolgen abrufen</span><span class="sxs-lookup"><span data-stu-id="30f29-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="30f29-110">Ruft die Verbindungszeichenfolgen für alle Schlüssel für den Iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="30f29-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="30f29-111">Beispiel 2 Abrufen der IotHub-Verbindungszeichenfolgen für einen bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="30f29-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="30f29-112">Ruft die Verbindungszeichenfolgen für den Schlüssel mit dem Namen "mykey" für den Iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="30f29-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="30f29-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30f29-113">PARAMETERS</span></span>

### <span data-ttu-id="30f29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f29-114">-DefaultProfile</span></span>
<span data-ttu-id="30f29-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="30f29-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30f29-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="30f29-116">-KeyName</span></span>
<span data-ttu-id="30f29-117">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="30f29-117">Name of the Key</span></span>

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

### <span data-ttu-id="30f29-118">-Name</span><span class="sxs-lookup"><span data-stu-id="30f29-118">-Name</span></span>
<span data-ttu-id="30f29-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="30f29-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="30f29-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f29-120">-ResourceGroupName</span></span>
<span data-ttu-id="30f29-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="30f29-121">Resource Group Name</span></span>

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

### <span data-ttu-id="30f29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f29-122">CommonParameters</span></span>
<span data-ttu-id="30f29-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f29-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f29-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f29-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30f29-125">INPUTS</span></span>

### <span data-ttu-id="30f29-126">System.String</span><span class="sxs-lookup"><span data-stu-id="30f29-126">System.String</span></span>

## <span data-ttu-id="30f29-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30f29-127">OUTPUTS</span></span>

### <span data-ttu-id="30f29-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="30f29-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="30f29-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30f29-129">NOTES</span></span>

## <span data-ttu-id="30f29-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30f29-130">RELATED LINKS</span></span>
