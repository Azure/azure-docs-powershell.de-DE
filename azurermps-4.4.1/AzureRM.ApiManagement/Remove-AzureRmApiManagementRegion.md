---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477410"
---
# <span data-ttu-id="dbe2a-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dbe2a-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="dbe2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbe2a-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe2a-103">Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbe2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbe2a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbe2a-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe2a-106">Das Cmdlet **Remove-AzureRmApiManagementRegion** entfernt eine Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** , die die Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="dbe2a-107">Dieses Cmdlet ändert die Bereitstellung nicht selbst, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="dbe2a-108">Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie den geänderten **PsApiManagementInstance** an **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="dbe2a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbe2a-109">EXAMPLES</span></span>

### <span data-ttu-id="dbe2a-110">Beispiel 1: Entfernen eines Bereichs aus einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="dbe2a-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="dbe2a-111">Mit diesem Befehl wird die Region East US aus der **PsApiManagement** -Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="dbe2a-112">Beispiel 2: Entfernen eines Bereichs aus einer PsApiManagement-Instanz mithilfe einer Reihe von Befehlen</span><span class="sxs-lookup"><span data-stu-id="dbe2a-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="dbe2a-113">Dieser erste Befehl ruft eine Instanz von **PsApiManagement** aus der Ressourcengruppe namens Contoso mit dem Namen ContosoApi ab.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="dbe2a-114">Der endgültige Befehl entfernt dann die Region mit dem Namen East US aus dieser Instanz und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="dbe2a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbe2a-115">PARAMETERS</span></span>

### <span data-ttu-id="dbe2a-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dbe2a-116">-ApiManagement</span></span>
<span data-ttu-id="dbe2a-117">Gibt die **PsApiManagement** -Instanz an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe2a-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="dbe2a-118">-Location</span></span>
<span data-ttu-id="dbe2a-119">Gibt den Speicherort des Bereichs an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="dbe2a-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="dbe2a-120">Valid values are:</span></span> 

- <span data-ttu-id="dbe2a-121">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="dbe2a-121">North Central US</span></span>
- <span data-ttu-id="dbe2a-122">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="dbe2a-122">South Central US</span></span>
- <span data-ttu-id="dbe2a-123">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="dbe2a-123">Central US</span></span>
- <span data-ttu-id="dbe2a-124">West Europa</span><span class="sxs-lookup"><span data-stu-id="dbe2a-124">West Europe</span></span>
- <span data-ttu-id="dbe2a-125">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="dbe2a-125">North Europe</span></span>
- <span data-ttu-id="dbe2a-126">West-US</span><span class="sxs-lookup"><span data-stu-id="dbe2a-126">West US</span></span>
- <span data-ttu-id="dbe2a-127">East US</span><span class="sxs-lookup"><span data-stu-id="dbe2a-127">East US</span></span>
- <span data-ttu-id="dbe2a-128">East US 2</span><span class="sxs-lookup"><span data-stu-id="dbe2a-128">East US 2</span></span>
- <span data-ttu-id="dbe2a-129">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="dbe2a-129">Japan East</span></span>
- <span data-ttu-id="dbe2a-130">Japan West</span><span class="sxs-lookup"><span data-stu-id="dbe2a-130">Japan West</span></span>
- <span data-ttu-id="dbe2a-131">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="dbe2a-131">Brazil South</span></span>
- <span data-ttu-id="dbe2a-132">Südostasien</span><span class="sxs-lookup"><span data-stu-id="dbe2a-132">Southeast Asia</span></span>
- <span data-ttu-id="dbe2a-133">Ostasien</span><span class="sxs-lookup"><span data-stu-id="dbe2a-133">East Asia</span></span>
- <span data-ttu-id="dbe2a-134">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="dbe2a-134">Australia East</span></span>
- <span data-ttu-id="dbe2a-135">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="dbe2a-135">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbe2a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe2a-136">-DefaultProfile</span></span>
<span data-ttu-id="dbe2a-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbe2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe2a-138">CommonParameters</span></span>
<span data-ttu-id="dbe2a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe2a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe2a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe2a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbe2a-141">INPUTS</span></span>

### <span data-ttu-id="dbe2a-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dbe2a-142">PsApiManagement</span></span>
<span data-ttu-id="dbe2a-143">Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbe2a-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="dbe2a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbe2a-144">OUTPUTS</span></span>

### <span data-ttu-id="dbe2a-145">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dbe2a-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dbe2a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbe2a-146">NOTES</span></span>

## <span data-ttu-id="dbe2a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbe2a-147">RELATED LINKS</span></span>

[<span data-ttu-id="dbe2a-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dbe2a-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="dbe2a-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="dbe2a-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


