---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303081"
---
# <span data-ttu-id="ece6e-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ece6e-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="ece6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ece6e-102">SYNOPSIS</span></span>
<span data-ttu-id="ece6e-103">Der **Test-AzPrivateLinkServiceVisibility** überprüft, ob ein privater Link Dienst für die aktuelle Verwendung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ece6e-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="ece6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece6e-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ece6e-105">DESCRIPTION</span></span>
<span data-ttu-id="ece6e-106">Überprüfen Sie, ob ein privater Link Dienst für die aktuelle Nutzung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ece6e-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="ece6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ece6e-107">EXAMPLES</span></span>

### <span data-ttu-id="ece6e-108">Beispiel 1: Überprüfen Sie, ob contoso.cloudapp.Azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ece6e-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="ece6e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ece6e-109">PARAMETERS</span></span>

### <span data-ttu-id="ece6e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece6e-110">-DefaultProfile</span></span>
<span data-ttu-id="ece6e-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ece6e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece6e-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="ece6e-112">-Location</span></span>
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

### <span data-ttu-id="ece6e-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="ece6e-113">-PrivateLinkServiceAlias</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece6e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece6e-114">-ResourceGroupName</span></span>
<span data-ttu-id="ece6e-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ece6e-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece6e-116">CommonParameters</span></span>
<span data-ttu-id="ece6e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece6e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece6e-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ece6e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece6e-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ece6e-119">INPUTS</span></span>

### <span data-ttu-id="ece6e-120">Keine</span><span class="sxs-lookup"><span data-stu-id="ece6e-120">None</span></span>

## <span data-ttu-id="ece6e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ece6e-121">OUTPUTS</span></span>

### <span data-ttu-id="ece6e-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ece6e-122">System.Boolean</span></span>

## <span data-ttu-id="ece6e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="ece6e-123">NOTES</span></span>

## <span data-ttu-id="ece6e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ece6e-124">RELATED LINKS</span></span>
