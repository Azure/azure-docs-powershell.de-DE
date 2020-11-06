---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478054"
---
# <span data-ttu-id="471f8-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="471f8-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="471f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="471f8-102">SYNOPSIS</span></span>
<span data-ttu-id="471f8-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="471f8-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="471f8-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="471f8-105">DESCRIPTION</span></span>
<span data-ttu-id="471f8-106">Das Cmdlet " **Satz-AzureRmApiManagementGroup** " konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="471f8-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="471f8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="471f8-107">EXAMPLES</span></span>

### <span data-ttu-id="471f8-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="471f8-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="471f8-109">Dieser Befehl konfiguriert eine Verwaltungsgruppe mit dem Namen Group0001.</span><span class="sxs-lookup"><span data-stu-id="471f8-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="471f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="471f8-110">PARAMETERS</span></span>

### <span data-ttu-id="471f8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="471f8-111">-Context</span></span>
<span data-ttu-id="471f8-112">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="471f8-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471f8-113">-DefaultProfile</span></span>
<span data-ttu-id="471f8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="471f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471f8-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="471f8-115">-Description</span></span>
<span data-ttu-id="471f8-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="471f8-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="471f8-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="471f8-117">-GroupId</span></span>
<span data-ttu-id="471f8-118">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="471f8-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="471f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="471f8-119">-Name</span></span>
<span data-ttu-id="471f8-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="471f8-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="471f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="471f8-121">-PassThru</span></span>
<span data-ttu-id="471f8-122">passthru</span><span class="sxs-lookup"><span data-stu-id="471f8-122">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="471f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471f8-123">CommonParameters</span></span>
<span data-ttu-id="471f8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="471f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471f8-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="471f8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471f8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="471f8-126">INPUTS</span></span>

### <span data-ttu-id="471f8-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="471f8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="471f8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="471f8-128">System.String</span></span>

### <span data-ttu-id="471f8-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="471f8-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="471f8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="471f8-130">OUTPUTS</span></span>

### <span data-ttu-id="471f8-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="471f8-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="471f8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="471f8-132">NOTES</span></span>

## <span data-ttu-id="471f8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="471f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="471f8-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="471f8-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="471f8-135">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="471f8-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="471f8-136">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="471f8-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


