---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503290"
---
# <span data-ttu-id="cd4bd-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cd4bd-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="cd4bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4bd-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd4bd-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd4bd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4bd-106">Das Cmdlet " **Satz-AzureRmApiManagementGroup** " konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="cd4bd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd4bd-107">EXAMPLES</span></span>

### <span data-ttu-id="cd4bd-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cd4bd-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="cd4bd-109">Dieser Befehl konfiguriert eine Verwaltungsgruppe mit dem Namen Group0001.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="cd4bd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd4bd-110">PARAMETERS</span></span>

### <span data-ttu-id="cd4bd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cd4bd-111">-Context</span></span>
<span data-ttu-id="cd4bd-112">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cd4bd-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd4bd-113">-Description</span></span>
<span data-ttu-id="cd4bd-114">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="cd4bd-115">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="cd4bd-115">-GroupId</span></span>
<span data-ttu-id="cd4bd-116">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="cd4bd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cd4bd-117">-Name</span></span>
<span data-ttu-id="cd4bd-118">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="cd4bd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd4bd-119">-PassThru</span></span>
<span data-ttu-id="cd4bd-120">passthru</span><span class="sxs-lookup"><span data-stu-id="cd4bd-120">passthru</span></span>

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

### <span data-ttu-id="cd4bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4bd-121">-DefaultProfile</span></span>
<span data-ttu-id="cd4bd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd4bd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4bd-123">CommonParameters</span></span>
<span data-ttu-id="cd4bd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd4bd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4bd-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4bd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4bd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd4bd-126">INPUTS</span></span>

## <span data-ttu-id="cd4bd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd4bd-127">OUTPUTS</span></span>

### <span data-ttu-id="cd4bd-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cd4bd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="cd4bd-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd4bd-129">NOTES</span></span>

## <span data-ttu-id="cd4bd-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd4bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="cd4bd-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cd4bd-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="cd4bd-132">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cd4bd-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="cd4bd-133">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cd4bd-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


