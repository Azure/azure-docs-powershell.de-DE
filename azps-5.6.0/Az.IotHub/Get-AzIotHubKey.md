---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 4a63f13e567a5f53726058c831107ce43768c0f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936859"
---
# <span data-ttu-id="ba3dd-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ba3dd-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="ba3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3dd-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="ba3dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba3dd-104">SYNTAX</span></span>

### <span data-ttu-id="ba3dd-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba3dd-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba3dd-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ba3dd-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba3dd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="ba3dd-108">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="ba3dd-109">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="ba3dd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="ba3dd-111">Beispiel 1 Alle Tasten erhalten</span><span class="sxs-lookup"><span data-stu-id="ba3dd-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ba3dd-112">Ruft alle Schlüssel für den IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ba3dd-113">Beispiel 2 Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="ba3dd-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="ba3dd-114">Ruft die Informationen für einen Schlüssel namens "iothubowner" für den IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ba3dd-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba3dd-115">PARAMETERS</span></span>

### <span data-ttu-id="ba3dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3dd-116">-DefaultProfile</span></span>
<span data-ttu-id="ba3dd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ba3dd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba3dd-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="ba3dd-118">-HubId</span></span>
<span data-ttu-id="ba3dd-119">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ba3dd-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3dd-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ba3dd-120">-KeyName</span></span>
<span data-ttu-id="ba3dd-121">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ba3dd-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3dd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ba3dd-122">-Name</span></span>
<span data-ttu-id="ba3dd-123">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba3dd-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ba3dd-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3dd-126">CommonParameters</span></span>
<span data-ttu-id="ba3dd-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3dd-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3dd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3dd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba3dd-129">INPUTS</span></span>

### <span data-ttu-id="ba3dd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ba3dd-130">System.String</span></span>

## <span data-ttu-id="ba3dd-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba3dd-131">OUTPUTS</span></span>

### <span data-ttu-id="ba3dd-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba3dd-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ba3dd-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba3dd-133">NOTES</span></span>

## <span data-ttu-id="ba3dd-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba3dd-134">RELATED LINKS</span></span>
