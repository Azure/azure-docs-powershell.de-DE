---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480513"
---
# <span data-ttu-id="ad391-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ad391-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="ad391-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad391-102">SYNOPSIS</span></span>
<span data-ttu-id="ad391-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="ad391-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad391-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad391-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad391-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad391-105">DESCRIPTION</span></span>
<span data-ttu-id="ad391-106">Das Cmdlet " **Get-AzureRmContainerService** " Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="ad391-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="ad391-107">Sie können die Eigenschaften eines Container Diensts anzeigen, der den Status, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamenmaster und Agent umfasst.</span><span class="sxs-lookup"><span data-stu-id="ad391-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="ad391-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad391-108">EXAMPLES</span></span>

### <span data-ttu-id="ad391-109">Beispiel 1: Abrufen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="ad391-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="ad391-110">Dieser Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="ad391-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="ad391-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad391-111">PARAMETERS</span></span>

### <span data-ttu-id="ad391-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad391-112">-DefaultProfile</span></span>
<span data-ttu-id="ad391-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad391-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad391-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ad391-114">-Name</span></span>
<span data-ttu-id="ad391-115">Gibt den Namen des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ad391-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad391-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad391-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad391-117">Gibt die Ressourcengruppe des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ad391-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad391-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad391-118">CommonParameters</span></span>
<span data-ttu-id="ad391-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad391-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad391-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad391-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad391-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad391-121">INPUTS</span></span>

### <span data-ttu-id="ad391-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ad391-122">System.String</span></span>

## <span data-ttu-id="ad391-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad391-123">OUTPUTS</span></span>

### <span data-ttu-id="ad391-124">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="ad391-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="ad391-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad391-125">NOTES</span></span>

## <span data-ttu-id="ad391-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad391-126">RELATED LINKS</span></span>

[<span data-ttu-id="ad391-127">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ad391-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="ad391-128">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ad391-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="ad391-129">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ad391-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


