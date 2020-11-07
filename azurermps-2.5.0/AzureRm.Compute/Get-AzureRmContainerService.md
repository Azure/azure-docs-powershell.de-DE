---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850940"
---
# <span data-ttu-id="cb26c-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cb26c-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="cb26c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb26c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb26c-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="cb26c-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb26c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb26c-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb26c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb26c-105">DESCRIPTION</span></span>
<span data-ttu-id="cb26c-106">Das Cmdlet " **Get-AzureRmContainerService** " Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="cb26c-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="cb26c-107">Sie können die Eigenschaften eines Container Diensts anzeigen, der den Status, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamenmaster und Agent umfasst.</span><span class="sxs-lookup"><span data-stu-id="cb26c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="cb26c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb26c-108">EXAMPLES</span></span>

### <span data-ttu-id="cb26c-109">Beispiel 1: Abrufen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="cb26c-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="cb26c-110">Dieser Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="cb26c-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="cb26c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb26c-111">PARAMETERS</span></span>

### <span data-ttu-id="cb26c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb26c-112">-DefaultProfile</span></span>
<span data-ttu-id="cb26c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb26c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb26c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cb26c-114">-Name</span></span>
<span data-ttu-id="cb26c-115">Gibt den Namen des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cb26c-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb26c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb26c-116">-ResourceGroupName</span></span>
<span data-ttu-id="cb26c-117">Gibt die Ressourcengruppe des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="cb26c-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb26c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb26c-118">CommonParameters</span></span>
<span data-ttu-id="cb26c-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb26c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb26c-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb26c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb26c-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb26c-121">INPUTS</span></span>

### <span data-ttu-id="cb26c-122">Keine</span><span class="sxs-lookup"><span data-stu-id="cb26c-122">None</span></span>
<span data-ttu-id="cb26c-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cb26c-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb26c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb26c-124">OUTPUTS</span></span>

### <span data-ttu-id="cb26c-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="cb26c-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="cb26c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb26c-126">NOTES</span></span>

## <span data-ttu-id="cb26c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb26c-127">RELATED LINKS</span></span>

[<span data-ttu-id="cb26c-128">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cb26c-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="cb26c-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cb26c-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="cb26c-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cb26c-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


