---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819788"
---
# <span data-ttu-id="82fc9-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="82fc9-101">Get-AzIotHub</span></span>

## <span data-ttu-id="82fc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="82fc9-103">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="82fc9-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="82fc9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82fc9-104">SYNTAX</span></span>

### <span data-ttu-id="82fc9-105">ListIotHubsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="82fc9-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82fc9-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="82fc9-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82fc9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82fc9-107">DESCRIPTION</span></span>
<span data-ttu-id="82fc9-108">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="82fc9-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="82fc9-109">Sie können alle IotHub-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten IotHub-Namen filtern.</span><span class="sxs-lookup"><span data-stu-id="82fc9-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="82fc9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82fc9-110">EXAMPLES</span></span>

### <span data-ttu-id="82fc9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82fc9-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="82fc9-112">Ruft alle IotHubs des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="82fc9-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="82fc9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="82fc9-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="82fc9-114">Ruft alle IotHubs in dem Abonnement ab, die der ResourceGroup mit dem Namen "myresourcegroup" angehören.</span><span class="sxs-lookup"><span data-stu-id="82fc9-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="82fc9-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="82fc9-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="82fc9-116">Ruft Informationen über die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="82fc9-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="82fc9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="82fc9-117">PARAMETERS</span></span>

### <span data-ttu-id="82fc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fc9-118">-DefaultProfile</span></span>
<span data-ttu-id="82fc9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="82fc9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82fc9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="82fc9-120">-Name</span></span>
<span data-ttu-id="82fc9-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="82fc9-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="82fc9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82fc9-122">-ResourceGroupName</span></span>
<span data-ttu-id="82fc9-123">Name der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="82fc9-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="82fc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fc9-124">CommonParameters</span></span>
<span data-ttu-id="82fc9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82fc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fc9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82fc9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fc9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82fc9-127">INPUTS</span></span>

### <span data-ttu-id="82fc9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="82fc9-128">System.String</span></span>

## <span data-ttu-id="82fc9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82fc9-129">OUTPUTS</span></span>

### <span data-ttu-id="82fc9-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="82fc9-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="82fc9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="82fc9-131">NOTES</span></span>

## <span data-ttu-id="82fc9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82fc9-132">RELATED LINKS</span></span>
