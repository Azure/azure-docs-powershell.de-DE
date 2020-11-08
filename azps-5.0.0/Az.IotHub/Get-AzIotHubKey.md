---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177948"
---
# <span data-ttu-id="fafbc-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="fafbc-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="fafbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fafbc-102">SYNOPSIS</span></span>
<span data-ttu-id="fafbc-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="fafbc-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="fafbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fafbc-104">SYNTAX</span></span>

### <span data-ttu-id="fafbc-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fafbc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fafbc-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fafbc-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fafbc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fafbc-107">DESCRIPTION</span></span>
<span data-ttu-id="fafbc-108">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="fafbc-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="fafbc-109">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="fafbc-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="fafbc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fafbc-110">EXAMPLES</span></span>

### <span data-ttu-id="fafbc-111">Beispiel 1 Abrufen aller Schlüssel</span><span class="sxs-lookup"><span data-stu-id="fafbc-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fafbc-112">Ruft alle Schlüssel für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="fafbc-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="fafbc-113">Beispiel 2 Abrufen von Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="fafbc-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="fafbc-114">Ruft die Informationen für einen Schlüssel mit dem Namen "iothubowner" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="fafbc-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fafbc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fafbc-115">PARAMETERS</span></span>

### <span data-ttu-id="fafbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafbc-116">-DefaultProfile</span></span>
<span data-ttu-id="fafbc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fafbc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fafbc-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="fafbc-118">-HubId</span></span>
<span data-ttu-id="fafbc-119">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fafbc-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fafbc-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fafbc-120">-KeyName</span></span>
<span data-ttu-id="fafbc-121">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="fafbc-121">Name of the Key</span></span>

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

### <span data-ttu-id="fafbc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fafbc-122">-Name</span></span>
<span data-ttu-id="fafbc-123">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="fafbc-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="fafbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="fafbc-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fafbc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fafbc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafbc-126">CommonParameters</span></span>
<span data-ttu-id="fafbc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafbc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafbc-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fafbc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafbc-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fafbc-129">INPUTS</span></span>

### <span data-ttu-id="fafbc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fafbc-130">System.String</span></span>

## <span data-ttu-id="fafbc-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fafbc-131">OUTPUTS</span></span>

### <span data-ttu-id="fafbc-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fafbc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="fafbc-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fafbc-133">NOTES</span></span>

## <span data-ttu-id="fafbc-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fafbc-134">RELATED LINKS</span></span>
