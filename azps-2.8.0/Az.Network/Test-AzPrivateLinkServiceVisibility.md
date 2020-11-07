---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823703"
---
# <span data-ttu-id="3ac5b-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="3ac5b-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="3ac5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ac5b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac5b-103">Der **Test-AzPrivateLinkServiceVisibility** überprüft, ob ein privater Link Dienst für die aktuelle Verwendung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="3ac5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ac5b-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ac5b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac5b-106">Überprüfen Sie, ob ein privater Link Dienst für die aktuelle Nutzung sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="3ac5b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ac5b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ac5b-108">Beispiel 1: Überprüfen Sie, ob contoso.cloudapp.Azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="3ac5b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ac5b-109">PARAMETERS</span></span>

### <span data-ttu-id="3ac5b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac5b-110">-DefaultProfile</span></span>
<span data-ttu-id="3ac5b-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac5b-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="3ac5b-112">-Location</span></span>
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

### <span data-ttu-id="3ac5b-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="3ac5b-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="3ac5b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac5b-114">-ResourceGroupName</span></span>
<span data-ttu-id="3ac5b-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3ac5b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac5b-116">CommonParameters</span></span>
<span data-ttu-id="3ac5b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac5b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac5b-118">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ac5b-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac5b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ac5b-119">INPUTS</span></span>

### <span data-ttu-id="3ac5b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="3ac5b-120">None</span></span>

## <span data-ttu-id="3ac5b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ac5b-121">OUTPUTS</span></span>

### <span data-ttu-id="3ac5b-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ac5b-122">System.Boolean</span></span>

## <span data-ttu-id="3ac5b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ac5b-123">NOTES</span></span>

## <span data-ttu-id="3ac5b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ac5b-124">RELATED LINKS</span></span>
