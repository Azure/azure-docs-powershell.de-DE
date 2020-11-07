---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: cc890bf13922069ac9f4d20d6a9e8d0c3aa04c94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843403"
---
# <span data-ttu-id="e825c-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e825c-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="e825c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e825c-102">SYNOPSIS</span></span>
<span data-ttu-id="e825c-103">Ruft einen Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="e825c-103">Gets a resource provider.</span></span>

## <span data-ttu-id="e825c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e825c-104">SYNTAX</span></span>

### <span data-ttu-id="e825c-105">ListAvailable (Standard)</span><span class="sxs-lookup"><span data-stu-id="e825c-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e825c-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="e825c-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e825c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e825c-107">DESCRIPTION</span></span>
<span data-ttu-id="e825c-108">Das Cmdlet " **Get-AzResourceProvider** " Ruft einen Azure-Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="e825c-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="e825c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e825c-109">EXAMPLES</span></span>

## <span data-ttu-id="e825c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e825c-110">PARAMETERS</span></span>

### <span data-ttu-id="e825c-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e825c-111">-ApiVersion</span></span>
<span data-ttu-id="e825c-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e825c-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e825c-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="e825c-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e825c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e825c-114">-DefaultProfile</span></span>
<span data-ttu-id="e825c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e825c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e825c-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e825c-116">-ListAvailable</span></span>
<span data-ttu-id="e825c-117">Gibt an, dass dieser Vorgang alle verfügbaren Ressourcenanbieter abruft.</span><span class="sxs-lookup"><span data-stu-id="e825c-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="e825c-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e825c-118">-Location</span></span>
<span data-ttu-id="e825c-119">Gibt den Speicherort des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="e825c-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="e825c-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="e825c-120">-Pre</span></span>
<span data-ttu-id="e825c-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e825c-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e825c-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e825c-122">-ProviderNamespace</span></span>
<span data-ttu-id="e825c-123">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="e825c-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e825c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e825c-124">CommonParameters</span></span>
<span data-ttu-id="e825c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e825c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e825c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e825c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e825c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e825c-127">INPUTS</span></span>

## <span data-ttu-id="e825c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e825c-128">OUTPUTS</span></span>

## <span data-ttu-id="e825c-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e825c-129">NOTES</span></span>

## <span data-ttu-id="e825c-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e825c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e825c-131">Registrieren-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e825c-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="e825c-132">Registrierung aufheben-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e825c-132">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


