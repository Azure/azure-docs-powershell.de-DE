---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504925"
---
# <span data-ttu-id="b2386-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="b2386-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="b2386-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2386-102">SYNOPSIS</span></span>
<span data-ttu-id="b2386-103">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b2386-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2386-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2386-104">SYNTAX</span></span>

### <span data-ttu-id="b2386-105">ListIotHubsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2386-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2386-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="b2386-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2386-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2386-107">DESCRIPTION</span></span>
<span data-ttu-id="b2386-108">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b2386-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="b2386-109">Sie können alle IotHub-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten IotHub-Namen filtern.</span><span class="sxs-lookup"><span data-stu-id="b2386-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="b2386-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2386-110">EXAMPLES</span></span>

### <span data-ttu-id="b2386-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2386-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="b2386-112">Ruft alle IotHubs des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="b2386-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="b2386-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b2386-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="b2386-114">Ruft alle IotHubs in dem Abonnement ab, die der ResourceGroup mit dem Namen "myresourcegroup" angehören.</span><span class="sxs-lookup"><span data-stu-id="b2386-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="b2386-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b2386-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b2386-116">Ruft Informationen über die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="b2386-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="b2386-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2386-117">PARAMETERS</span></span>

### <span data-ttu-id="b2386-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b2386-118">-Name</span></span>
<span data-ttu-id="b2386-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="b2386-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2386-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2386-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2386-121">Name der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2386-121">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2386-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2386-122">-DefaultProfile</span></span>
<span data-ttu-id="b2386-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2386-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2386-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2386-124">CommonParameters</span></span>
<span data-ttu-id="b2386-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2386-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2386-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2386-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2386-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2386-127">INPUTS</span></span>

### <span data-ttu-id="b2386-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b2386-128">System.String</span></span>

## <span data-ttu-id="b2386-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2386-129">OUTPUTS</span></span>

### <span data-ttu-id="b2386-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b2386-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="b2386-131">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="b2386-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="b2386-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2386-132">NOTES</span></span>

## <span data-ttu-id="b2386-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2386-133">RELATED LINKS</span></span>

