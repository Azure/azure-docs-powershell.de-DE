---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472405"
---
# <span data-ttu-id="9e6c4-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="9e6c4-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="9e6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6c4-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="9e6c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e6c4-104">SYNTAX</span></span>

### <span data-ttu-id="9e6c4-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e6c4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e6c4-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9e6c4-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e6c4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="9e6c4-108">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="9e6c4-109">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="9e6c4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e6c4-110">EXAMPLES</span></span>

### <span data-ttu-id="9e6c4-111">Beispiel 1: Alle Schlüssel erhalten</span><span class="sxs-lookup"><span data-stu-id="9e6c4-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9e6c4-112">Ruft alle Schlüssel für IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="9e6c4-113">Beispiel 2: Informationen zu einem bestimmten Schlüssel erhalten</span><span class="sxs-lookup"><span data-stu-id="9e6c4-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="9e6c4-114">Ruft die Informationen für einen Schlüssel namens "iothubowner" für IotHub namens "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9e6c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e6c4-115">PARAMETERS</span></span>

### <span data-ttu-id="9e6c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6c4-116">-DefaultProfile</span></span>
<span data-ttu-id="9e6c4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9e6c4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e6c4-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="9e6c4-118">-HubId</span></span>
<span data-ttu-id="9e6c4-119">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="9e6c4-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9e6c4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9e6c4-120">-KeyName</span></span>
<span data-ttu-id="9e6c4-121">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="9e6c4-121">Name of the Key</span></span>

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

### <span data-ttu-id="9e6c4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9e6c4-122">-Name</span></span>
<span data-ttu-id="9e6c4-123">Name des IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="9e6c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e6c4-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="9e6c4-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9e6c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6c4-126">CommonParameters</span></span>
<span data-ttu-id="9e6c4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6c4-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6c4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6c4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e6c4-129">INPUTS</span></span>

### <span data-ttu-id="9e6c4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9e6c4-130">System.String</span></span>

## <span data-ttu-id="9e6c4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e6c4-131">OUTPUTS</span></span>

### <span data-ttu-id="9e6c4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9e6c4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="9e6c4-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e6c4-133">NOTES</span></span>

## <span data-ttu-id="9e6c4-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e6c4-134">RELATED LINKS</span></span>
