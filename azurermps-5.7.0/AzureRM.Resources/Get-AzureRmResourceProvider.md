---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 54ce1d9fa73b29318597f5a1442712aabf7f92b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476610"
---
# <span data-ttu-id="96487-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="96487-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="96487-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96487-102">SYNOPSIS</span></span>
<span data-ttu-id="96487-103">Ruft einen Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="96487-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96487-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96487-104">SYNTAX</span></span>

### <span data-ttu-id="96487-105">ListAvailable (Standard)</span><span class="sxs-lookup"><span data-stu-id="96487-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96487-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="96487-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96487-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96487-107">DESCRIPTION</span></span>
<span data-ttu-id="96487-108">Das Cmdlet " **Get-AzureRmResourceProvider** " Ruft einen Azure-Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="96487-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="96487-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96487-109">EXAMPLES</span></span>

## <span data-ttu-id="96487-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96487-110">PARAMETERS</span></span>

### <span data-ttu-id="96487-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="96487-111">-ApiVersion</span></span>
<span data-ttu-id="96487-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="96487-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="96487-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="96487-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96487-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96487-114">-DefaultProfile</span></span>
<span data-ttu-id="96487-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96487-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96487-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="96487-116">-ListAvailable</span></span>
<span data-ttu-id="96487-117">Gibt an, dass dieser Vorgang alle verfügbaren Ressourcenanbieter abruft.</span><span class="sxs-lookup"><span data-stu-id="96487-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96487-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="96487-118">-Location</span></span>
<span data-ttu-id="96487-119">Gibt den Speicherort des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="96487-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96487-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="96487-120">-Pre</span></span>
<span data-ttu-id="96487-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="96487-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96487-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="96487-122">-ProviderNamespace</span></span>
<span data-ttu-id="96487-123">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="96487-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96487-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96487-124">CommonParameters</span></span>
<span data-ttu-id="96487-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96487-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96487-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96487-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96487-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96487-127">INPUTS</span></span>

### <span data-ttu-id="96487-128">Keine</span><span class="sxs-lookup"><span data-stu-id="96487-128">None</span></span>
<span data-ttu-id="96487-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="96487-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96487-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96487-130">OUTPUTS</span></span>

### <span data-ttu-id="96487-131">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="96487-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="96487-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="96487-132">NOTES</span></span>

## <span data-ttu-id="96487-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96487-133">RELATED LINKS</span></span>

[<span data-ttu-id="96487-134">Registrieren-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="96487-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="96487-135">Registrierung aufheben-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="96487-135">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


