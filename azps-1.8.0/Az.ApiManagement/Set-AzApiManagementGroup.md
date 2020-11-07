---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820996"
---
# <span data-ttu-id="577f8-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="577f8-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="577f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="577f8-102">SYNOPSIS</span></span>
<span data-ttu-id="577f8-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="577f8-103">Configures an API management group.</span></span>

## <span data-ttu-id="577f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="577f8-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="577f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="577f8-105">DESCRIPTION</span></span>
<span data-ttu-id="577f8-106">Das Cmdlet " **Satz-AzApiManagementGroup** " konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="577f8-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="577f8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="577f8-107">EXAMPLES</span></span>

### <span data-ttu-id="577f8-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="577f8-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="577f8-109">Dieser Befehl konfiguriert eine Verwaltungsgruppe mit dem Namen Group0001.</span><span class="sxs-lookup"><span data-stu-id="577f8-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="577f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="577f8-110">PARAMETERS</span></span>

### <span data-ttu-id="577f8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="577f8-111">-Context</span></span>
<span data-ttu-id="577f8-112">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="577f8-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="577f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577f8-113">-DefaultProfile</span></span>
<span data-ttu-id="577f8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="577f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="577f8-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="577f8-115">-Description</span></span>
<span data-ttu-id="577f8-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="577f8-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="577f8-117">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="577f8-117">-GroupId</span></span>
<span data-ttu-id="577f8-118">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="577f8-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="577f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="577f8-119">-Name</span></span>
<span data-ttu-id="577f8-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="577f8-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="577f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="577f8-121">-PassThru</span></span>
<span data-ttu-id="577f8-122">passthru</span><span class="sxs-lookup"><span data-stu-id="577f8-122">passthru</span></span>

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

### <span data-ttu-id="577f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577f8-123">CommonParameters</span></span>
<span data-ttu-id="577f8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577f8-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577f8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577f8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="577f8-126">INPUTS</span></span>

### <span data-ttu-id="577f8-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="577f8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="577f8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="577f8-128">System.String</span></span>

### <span data-ttu-id="577f8-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="577f8-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="577f8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="577f8-130">OUTPUTS</span></span>

### <span data-ttu-id="577f8-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="577f8-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="577f8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="577f8-132">NOTES</span></span>

## <span data-ttu-id="577f8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="577f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="577f8-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="577f8-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="577f8-135">Neu – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="577f8-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="577f8-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="577f8-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


