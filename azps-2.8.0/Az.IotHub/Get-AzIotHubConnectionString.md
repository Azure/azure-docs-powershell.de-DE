---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f89d47dac0b48ca82b2478743d2993f94fb792d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650986"
---
# <span data-ttu-id="a1f0f-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="a1f0f-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="a1f0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f0f-103">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="a1f0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f0f-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f0f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="a1f0f-106">Ruft die IotHub-connectionStrings ab.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="a1f0f-107">Sie können entweder connectionStrings für alle Schlüssel abrufen oder nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="a1f0f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1f0f-108">EXAMPLES</span></span>

### <span data-ttu-id="a1f0f-109">Beispiel 1 Abrufen aller IotHub-connectionStrings</span><span class="sxs-lookup"><span data-stu-id="a1f0f-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a1f0f-110">Ruft die ConnectionStrings für alle Schlüssel für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="a1f0f-111">Beispiel 2 Abrufen der IotHub-connectionStrings für einen bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a1f0f-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="a1f0f-112">Ruft die ConnectionStrings für den Schlüssel mit dem Namen "MyKey" für die iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="a1f0f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f0f-113">PARAMETERS</span></span>

### <span data-ttu-id="a1f0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f0f-114">-DefaultProfile</span></span>
<span data-ttu-id="a1f0f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a1f0f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1f0f-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a1f0f-116">-KeyName</span></span>
<span data-ttu-id="a1f0f-117">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="a1f0f-117">Name of the Key</span></span>

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

### <span data-ttu-id="a1f0f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a1f0f-118">-Name</span></span>
<span data-ttu-id="a1f0f-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="a1f0f-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a1f0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1f0f-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a1f0f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a1f0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f0f-122">CommonParameters</span></span>
<span data-ttu-id="a1f0f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f0f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f0f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f0f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1f0f-125">INPUTS</span></span>

### <span data-ttu-id="a1f0f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a1f0f-126">System.String</span></span>

## <span data-ttu-id="a1f0f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1f0f-127">OUTPUTS</span></span>

### <span data-ttu-id="a1f0f-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a1f0f-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="a1f0f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1f0f-129">NOTES</span></span>

## <span data-ttu-id="a1f0f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1f0f-130">RELATED LINKS</span></span>
