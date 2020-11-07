---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c179ac3657a69b908c605fbaf4d0577b8a77a90f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843159"
---
# <span data-ttu-id="c68ba-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c68ba-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="c68ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c68ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c68ba-103">Hebt die Registrierung eines Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="c68ba-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="c68ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c68ba-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c68ba-105">DESCRIPTION</span></span>
<span data-ttu-id="c68ba-106">Das Cmdlet " **Unregister-AzResourceProvider** " hebt die Registrierung eines Azure-Ressourcenanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="c68ba-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="c68ba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c68ba-107">EXAMPLES</span></span>

## <span data-ttu-id="c68ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68ba-108">PARAMETERS</span></span>

### <span data-ttu-id="c68ba-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c68ba-109">-ApiVersion</span></span>
<span data-ttu-id="c68ba-110">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c68ba-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c68ba-111">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="c68ba-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c68ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68ba-112">-DefaultProfile</span></span>
<span data-ttu-id="c68ba-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c68ba-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c68ba-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="c68ba-114">-Pre</span></span>
<span data-ttu-id="c68ba-115">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c68ba-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c68ba-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c68ba-116">-ProviderNamespace</span></span>
<span data-ttu-id="c68ba-117">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="c68ba-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="c68ba-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c68ba-118">-Confirm</span></span>
<span data-ttu-id="c68ba-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c68ba-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68ba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68ba-120">-WhatIf</span></span>
<span data-ttu-id="c68ba-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c68ba-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68ba-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c68ba-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68ba-123">CommonParameters</span></span>
<span data-ttu-id="c68ba-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68ba-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68ba-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68ba-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c68ba-126">INPUTS</span></span>

## <span data-ttu-id="c68ba-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c68ba-127">OUTPUTS</span></span>

## <span data-ttu-id="c68ba-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c68ba-128">NOTES</span></span>

## <span data-ttu-id="c68ba-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c68ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="c68ba-130">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c68ba-130">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="c68ba-131">Registrieren-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c68ba-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


