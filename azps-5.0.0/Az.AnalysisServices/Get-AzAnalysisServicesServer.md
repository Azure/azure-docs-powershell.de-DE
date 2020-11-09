---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302301"
---
# <span data-ttu-id="ba316-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba316-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="ba316-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba316-102">SYNOPSIS</span></span>
<span data-ttu-id="ba316-103">Ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="ba316-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="ba316-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba316-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba316-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba316-105">DESCRIPTION</span></span>
<span data-ttu-id="ba316-106">Das Get-AzAnalysisServicesServer-Cmdlet ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="ba316-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="ba316-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba316-107">EXAMPLES</span></span>

### <span data-ttu-id="ba316-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba316-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="ba316-109">Dieser Befehl ruft alle Azure Analysis Services-Server in der Ressourcengruppe mit dem Namen ResourceGroup03 ab.</span><span class="sxs-lookup"><span data-stu-id="ba316-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="ba316-110">Beispiel 2: Abrufen eines Servers</span><span class="sxs-lookup"><span data-stu-id="ba316-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="ba316-111">Mit diesem Befehl wird der Azure Analysis Services-Server mit dem Namen Testserver in der Ressourcengruppe mit dem Namen ResourceGroup03 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba316-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="ba316-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba316-112">PARAMETERS</span></span>

### <span data-ttu-id="ba316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba316-113">-DefaultProfile</span></span>
<span data-ttu-id="ba316-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba316-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba316-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ba316-115">-Name</span></span>
<span data-ttu-id="ba316-116">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ba316-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ba316-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba316-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba316-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="ba316-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba316-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba316-119">CommonParameters</span></span>
<span data-ttu-id="ba316-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba316-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba316-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba316-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba316-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba316-122">INPUTS</span></span>

### <span data-ttu-id="ba316-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ba316-123">System.String</span></span>

## <span data-ttu-id="ba316-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba316-124">OUTPUTS</span></span>

### <span data-ttu-id="ba316-125">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba316-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="ba316-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba316-126">NOTES</span></span>
<span data-ttu-id="ba316-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="ba316-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="ba316-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba316-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba316-129">Neu – AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="ba316-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="ba316-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="ba316-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
