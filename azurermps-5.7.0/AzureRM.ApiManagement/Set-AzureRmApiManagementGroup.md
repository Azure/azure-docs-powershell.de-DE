---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496682"
---
# <span data-ttu-id="667b3-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="667b3-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="667b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="667b3-102">SYNOPSIS</span></span>
<span data-ttu-id="667b3-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="667b3-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="667b3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="667b3-105">DESCRIPTION</span></span>
<span data-ttu-id="667b3-106">Das Cmdlet " **Satz-AzureRmApiManagementGroup** " konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="667b3-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="667b3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="667b3-107">EXAMPLES</span></span>

### <span data-ttu-id="667b3-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="667b3-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="667b3-109">Dieser Befehl konfiguriert eine Verwaltungsgruppe mit dem Namen Group0001.</span><span class="sxs-lookup"><span data-stu-id="667b3-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="667b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="667b3-110">PARAMETERS</span></span>

### <span data-ttu-id="667b3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="667b3-111">-Context</span></span>
<span data-ttu-id="667b3-112">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="667b3-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667b3-113">-DefaultProfile</span></span>
<span data-ttu-id="667b3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="667b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="667b3-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="667b3-115">-Description</span></span>
<span data-ttu-id="667b3-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="667b3-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="667b3-117">-GroupId</span></span>
<span data-ttu-id="667b3-118">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="667b3-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="667b3-119">-Name</span></span>
<span data-ttu-id="667b3-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="667b3-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="667b3-121">-PassThru</span></span>
<span data-ttu-id="667b3-122">passthru</span><span class="sxs-lookup"><span data-stu-id="667b3-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667b3-123">CommonParameters</span></span>
<span data-ttu-id="667b3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667b3-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667b3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667b3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="667b3-126">INPUTS</span></span>

### <span data-ttu-id="667b3-127">Keine</span><span class="sxs-lookup"><span data-stu-id="667b3-127">None</span></span>
<span data-ttu-id="667b3-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="667b3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="667b3-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="667b3-129">OUTPUTS</span></span>

### <span data-ttu-id="667b3-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="667b3-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="667b3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="667b3-131">NOTES</span></span>

## <span data-ttu-id="667b3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="667b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="667b3-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="667b3-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="667b3-134">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="667b3-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="667b3-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="667b3-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


