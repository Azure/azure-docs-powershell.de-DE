---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 1076ff16005665aa81e4775507a236fe62bb0965
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843960"
---
# <span data-ttu-id="b70e3-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b70e3-101">Get-AzIotHub</span></span>

## <span data-ttu-id="b70e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b70e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b70e3-103">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b70e3-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="b70e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b70e3-104">SYNTAX</span></span>

### <span data-ttu-id="b70e3-105">ListIotHubsByResourceGroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="b70e3-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b70e3-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="b70e3-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b70e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b70e3-107">DESCRIPTION</span></span>
<span data-ttu-id="b70e3-108">Ruft Informationen zu den IotHubs in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b70e3-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="b70e3-109">Sie können alle IotHub-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten IotHub-Namen filtern.</span><span class="sxs-lookup"><span data-stu-id="b70e3-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="b70e3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b70e3-110">EXAMPLES</span></span>

### <span data-ttu-id="b70e3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b70e3-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="b70e3-112">Ruft alle IotHubs des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="b70e3-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="b70e3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b70e3-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="b70e3-114">Ruft alle IotHubs in dem Abonnement ab, die der ResourceGroup mit dem Namen "myresourcegroup" angehören.</span><span class="sxs-lookup"><span data-stu-id="b70e3-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="b70e3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b70e3-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b70e3-116">Ruft Informationen über die IotHub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="b70e3-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="b70e3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b70e3-117">PARAMETERS</span></span>

### <span data-ttu-id="b70e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70e3-118">-DefaultProfile</span></span>
<span data-ttu-id="b70e3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b70e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b70e3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b70e3-120">-Name</span></span>
<span data-ttu-id="b70e3-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="b70e3-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b70e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="b70e3-123">Name der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b70e3-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="b70e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70e3-124">CommonParameters</span></span>
<span data-ttu-id="b70e3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70e3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70e3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70e3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b70e3-127">INPUTS</span></span>

### <span data-ttu-id="b70e3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b70e3-128">System.String</span></span>

## <span data-ttu-id="b70e3-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b70e3-129">OUTPUTS</span></span>

### <span data-ttu-id="b70e3-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b70e3-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="b70e3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b70e3-131">NOTES</span></span>

## <span data-ttu-id="b70e3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b70e3-132">RELATED LINKS</span></span>
