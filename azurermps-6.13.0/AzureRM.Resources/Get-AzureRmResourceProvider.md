---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 8b7b4109441b10da0bf5c7f572c90f25a17293a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665119"
---
# <span data-ttu-id="1e0f9-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1e0f9-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="1e0f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0f9-103">Ruft einen Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e0f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e0f9-104">SYNTAX</span></span>

### <span data-ttu-id="1e0f9-105">ListAvailable (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e0f9-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0f9-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="1e0f9-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e0f9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e0f9-107">DESCRIPTION</span></span>
<span data-ttu-id="1e0f9-108">Das Cmdlet " **Get-AzureRmResourceProvider** " Ruft einen Azure-Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="1e0f9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e0f9-109">EXAMPLES</span></span>

## <span data-ttu-id="1e0f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e0f9-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0f9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e0f9-111">-ApiVersion</span></span>
<span data-ttu-id="1e0f9-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1e0f9-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1e0f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0f9-114">-DefaultProfile</span></span>
<span data-ttu-id="1e0f9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e0f9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e0f9-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="1e0f9-116">-ListAvailable</span></span>
<span data-ttu-id="1e0f9-117">Gibt an, dass dieser Vorgang alle verfügbaren Ressourcenanbieter abruft.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="1e0f9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="1e0f9-118">-Location</span></span>
<span data-ttu-id="1e0f9-119">Gibt den Speicherort des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="1e0f9-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="1e0f9-120">-Pre</span></span>
<span data-ttu-id="1e0f9-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1e0f9-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="1e0f9-122">-ProviderNamespace</span></span>
<span data-ttu-id="1e0f9-123">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="1e0f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0f9-124">CommonParameters</span></span>
<span data-ttu-id="1e0f9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0f9-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e0f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0f9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e0f9-127">INPUTS</span></span>

## <span data-ttu-id="1e0f9-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e0f9-128">OUTPUTS</span></span>

## <span data-ttu-id="1e0f9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e0f9-129">NOTES</span></span>

## <span data-ttu-id="1e0f9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e0f9-130">RELATED LINKS</span></span>

[<span data-ttu-id="1e0f9-131">Registrieren-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1e0f9-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="1e0f9-132">Registrierung aufheben-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1e0f9-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


