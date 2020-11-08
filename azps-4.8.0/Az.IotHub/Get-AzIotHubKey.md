---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175127"
---
# <span data-ttu-id="c3418-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="c3418-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="c3418-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3418-102">SYNOPSIS</span></span>
<span data-ttu-id="c3418-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="c3418-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="c3418-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3418-104">SYNTAX</span></span>

### <span data-ttu-id="c3418-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3418-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3418-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3418-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3418-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3418-107">DESCRIPTION</span></span>
<span data-ttu-id="c3418-108">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="c3418-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="c3418-109">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="c3418-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="c3418-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3418-110">EXAMPLES</span></span>

### <span data-ttu-id="c3418-111">Beispiel 1 Abrufen aller Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c3418-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c3418-112">Ruft alle Schlüssel für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="c3418-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="c3418-113">Beispiel 2 Abrufen von Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c3418-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="c3418-114">Ruft die Informationen für einen Schlüssel mit dem Namen "iothubowner" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="c3418-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c3418-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3418-115">PARAMETERS</span></span>

### <span data-ttu-id="c3418-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3418-116">-DefaultProfile</span></span>
<span data-ttu-id="c3418-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3418-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3418-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="c3418-118">-HubId</span></span>
<span data-ttu-id="c3418-119">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c3418-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c3418-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c3418-120">-KeyName</span></span>
<span data-ttu-id="c3418-121">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="c3418-121">Name of the Key</span></span>

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

### <span data-ttu-id="c3418-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3418-122">-Name</span></span>
<span data-ttu-id="c3418-123">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="c3418-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="c3418-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3418-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3418-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c3418-125">Resource Group Name</span></span>

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

### <span data-ttu-id="c3418-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3418-126">CommonParameters</span></span>
<span data-ttu-id="c3418-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3418-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3418-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3418-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3418-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3418-129">INPUTS</span></span>

### <span data-ttu-id="c3418-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c3418-130">System.String</span></span>

## <span data-ttu-id="c3418-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3418-131">OUTPUTS</span></span>

### <span data-ttu-id="c3418-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3418-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="c3418-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3418-133">NOTES</span></span>

## <span data-ttu-id="c3418-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3418-134">RELATED LINKS</span></span>
