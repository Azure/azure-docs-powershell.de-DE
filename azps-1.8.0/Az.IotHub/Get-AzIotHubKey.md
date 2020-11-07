---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819775"
---
# <span data-ttu-id="2339f-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="2339f-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="2339f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2339f-102">SYNOPSIS</span></span>
<span data-ttu-id="2339f-103">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="2339f-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="2339f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2339f-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2339f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2339f-105">DESCRIPTION</span></span>
<span data-ttu-id="2339f-106">Ruft einen IotHub-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="2339f-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="2339f-107">Sie können entweder alle Schlüssel auflisten oder die Liste nach einem bestimmten Schlüsselnamen filtern.</span><span class="sxs-lookup"><span data-stu-id="2339f-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="2339f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2339f-108">EXAMPLES</span></span>

### <span data-ttu-id="2339f-109">Beispiel 1 Abrufen aller Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2339f-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2339f-110">Ruft alle Schlüssel für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="2339f-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2339f-111">Beispiel 2 Abrufen von Informationen zu einem bestimmten Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2339f-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="2339f-112">Ruft die Informationen für einen Schlüssel mit dem Namen "iothubowner" für die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="2339f-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2339f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2339f-113">PARAMETERS</span></span>

### <span data-ttu-id="2339f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2339f-114">-DefaultProfile</span></span>
<span data-ttu-id="2339f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2339f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2339f-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2339f-116">-KeyName</span></span>
<span data-ttu-id="2339f-117">Name des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="2339f-117">Name of the Key</span></span>

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

### <span data-ttu-id="2339f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2339f-118">-Name</span></span>
<span data-ttu-id="2339f-119">Der Name des viel-Hubs.</span><span class="sxs-lookup"><span data-stu-id="2339f-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2339f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2339f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2339f-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2339f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2339f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2339f-122">CommonParameters</span></span>
<span data-ttu-id="2339f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2339f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2339f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2339f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2339f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2339f-125">INPUTS</span></span>

### <span data-ttu-id="2339f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2339f-126">System.String</span></span>

## <span data-ttu-id="2339f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2339f-127">OUTPUTS</span></span>

### <span data-ttu-id="2339f-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2339f-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="2339f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2339f-129">NOTES</span></span>

## <span data-ttu-id="2339f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2339f-130">RELATED LINKS</span></span>
