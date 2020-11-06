---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495573"
---
# <span data-ttu-id="8c11d-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="8c11d-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="8c11d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c11d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c11d-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl gibt die URL der fortlaufenden Container Bereitstellung zurück</span><span class="sxs-lookup"><span data-stu-id="8c11d-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c11d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c11d-104">SYNTAX</span></span>

### <span data-ttu-id="8c11d-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c11d-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c11d-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c11d-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c11d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c11d-107">DESCRIPTION</span></span>
<span data-ttu-id="8c11d-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl gibt die URL der fortlaufenden Container Bereitstellung zurück</span><span class="sxs-lookup"><span data-stu-id="8c11d-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="8c11d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c11d-109">EXAMPLES</span></span>

### <span data-ttu-id="8c11d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c11d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8c11d-111">Dieser Befehl gibt die Container-URL für die fortlaufende Bereitstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="8c11d-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="8c11d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c11d-112">PARAMETERS</span></span>

### <span data-ttu-id="8c11d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c11d-113">-DefaultProfile</span></span>
<span data-ttu-id="8c11d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c11d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c11d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8c11d-115">-Name</span></span>
<span data-ttu-id="8c11d-116">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="8c11d-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c11d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c11d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8c11d-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c11d-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c11d-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="8c11d-119">-SlotName</span></span>
<span data-ttu-id="8c11d-120">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="8c11d-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c11d-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="8c11d-121">-WebApp</span></span>
<span data-ttu-id="8c11d-122">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="8c11d-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c11d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c11d-123">CommonParameters</span></span>
<span data-ttu-id="8c11d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c11d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c11d-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c11d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c11d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c11d-126">INPUTS</span></span>

### <span data-ttu-id="8c11d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8c11d-127">System.String</span></span>
### <span data-ttu-id="8c11d-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8c11d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="8c11d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c11d-129">OUTPUTS</span></span>

### <span data-ttu-id="8c11d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c11d-130">System.String</span></span>
## <span data-ttu-id="8c11d-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c11d-131">NOTES</span></span>

## <span data-ttu-id="8c11d-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c11d-132">RELATED LINKS</span></span>
