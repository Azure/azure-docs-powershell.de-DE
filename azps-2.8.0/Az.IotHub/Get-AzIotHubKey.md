---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650978"
---
# <span data-ttu-id="b0b2d-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b0b2d-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="b0b2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b2d-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="b0b2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0b2d-104">SYNTAX</span></span>

### <span data-ttu-id="b0b2d-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0b2d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b2d-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0b2d-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0b2d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b2d-107">DESCRIPTION</span></span>
<span data-ttu-id="b0b2d-108">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="b0b2d-109">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="b0b2d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0b2d-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b2d-111">Beispiel 1 Abrufen aller Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b0b2d-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b0b2d-112">Ruft alle Schlüssel für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="b0b2d-113">Beispiel 2 Abrufen von Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b0b2d-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="b0b2d-114">Ruft die Informationen für einen Schlüssel mit dem Namen "iothubowner" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b0b2d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b2d-115">PARAMETERS</span></span>

### <span data-ttu-id="b0b2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b2d-116">-DefaultProfile</span></span>
<span data-ttu-id="b0b2d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b0b2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0b2d-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="b0b2d-118">-HubId</span></span>
<span data-ttu-id="b0b2d-119">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b0b2d-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b0b2d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b0b2d-120">-KeyName</span></span>
<span data-ttu-id="b0b2d-121">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="b0b2d-121">Name of the Key</span></span>

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

### <span data-ttu-id="b0b2d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b2d-122">-Name</span></span>
<span data-ttu-id="b0b2d-123">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b0b2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0b2d-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b0b2d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b0b2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b2d-126">CommonParameters</span></span>
<span data-ttu-id="b0b2d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b2d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b2d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b2d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0b2d-129">INPUTS</span></span>

### <span data-ttu-id="b0b2d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b0b2d-130">System.String</span></span>

## <span data-ttu-id="b0b2d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0b2d-131">OUTPUTS</span></span>

### <span data-ttu-id="b0b2d-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b0b2d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b0b2d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0b2d-133">NOTES</span></span>

## <span data-ttu-id="b0b2d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0b2d-134">RELATED LINKS</span></span>
