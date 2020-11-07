---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848379"
---
# <span data-ttu-id="3b3ca-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b3ca-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="3b3ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ca-103">Ruft einen Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b3ca-104">SYNTAX</span></span>

### <span data-ttu-id="3b3ca-105">ListAvailable (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b3ca-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b3ca-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="3b3ca-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b3ca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3ca-107">DESCRIPTION</span></span>
<span data-ttu-id="3b3ca-108">Das Cmdlet " **Get-AzureRmResourceProvider** " Ruft einen Azure-Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="3b3ca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b3ca-109">EXAMPLES</span></span>

## <span data-ttu-id="3b3ca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b3ca-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3ca-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3b3ca-111">-ApiVersion</span></span>
<span data-ttu-id="3b3ca-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3b3ca-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ca-114">-DefaultProfile</span></span>
<span data-ttu-id="3b3ca-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b3ca-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b3ca-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3b3ca-116">-ListAvailable</span></span>
<span data-ttu-id="3b3ca-117">Gibt an, dass dieser Vorgang alle verfügbaren Ressourcenanbieter abruft.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ca-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="3b3ca-118">-Location</span></span>
<span data-ttu-id="3b3ca-119">Gibt den Speicherort des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ca-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="3b3ca-120">-Pre</span></span>
<span data-ttu-id="3b3ca-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ca-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3b3ca-122">-ProviderNamespace</span></span>
<span data-ttu-id="3b3ca-123">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ca-124">CommonParameters</span></span>
<span data-ttu-id="3b3ca-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ca-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ca-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b3ca-127">INPUTS</span></span>

## <span data-ttu-id="3b3ca-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b3ca-128">OUTPUTS</span></span>

## <span data-ttu-id="3b3ca-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b3ca-129">NOTES</span></span>

## <span data-ttu-id="3b3ca-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b3ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ca-131">Registrieren-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b3ca-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="3b3ca-132">Registrierung aufheben-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3b3ca-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


