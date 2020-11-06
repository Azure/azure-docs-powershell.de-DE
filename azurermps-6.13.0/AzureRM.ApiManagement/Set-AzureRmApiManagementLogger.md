---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482590"
---
# <span data-ttu-id="3293f-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3293f-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="3293f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3293f-102">SYNOPSIS</span></span>
<span data-ttu-id="3293f-103">Ändert eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="3293f-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3293f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3293f-104">SYNTAX</span></span>

### <span data-ttu-id="3293f-105">EventHubLoggerSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3293f-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3293f-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="3293f-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3293f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3293f-107">DESCRIPTION</span></span>
<span data-ttu-id="3293f-108">Das Cmdlet " **festlegen-AzureRmApiManagementLogger** " ändert die Einstellungen einer Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="3293f-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="3293f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3293f-109">EXAMPLES</span></span>

### <span data-ttu-id="3293f-110">Beispiel 1: Ändern der EventHub-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="3293f-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="3293f-111">Mit diesem Befehl wird eine Protokollierung geändert, die die ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="3293f-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3293f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3293f-112">PARAMETERS</span></span>

### <span data-ttu-id="3293f-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3293f-113">-ConnectionString</span></span>
<span data-ttu-id="3293f-114">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die Sende Richtlinienrechte umfasst.</span><span class="sxs-lookup"><span data-stu-id="3293f-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3293f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="3293f-115">-Context</span></span>
<span data-ttu-id="3293f-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3293f-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3293f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3293f-117">-DefaultProfile</span></span>
<span data-ttu-id="3293f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3293f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3293f-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3293f-119">-Description</span></span>
<span data-ttu-id="3293f-120">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="3293f-120">Specifies a description.</span></span>

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

### <span data-ttu-id="3293f-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="3293f-121">-InstrumentationKey</span></span>
<span data-ttu-id="3293f-122">Instrumentations Schlüssel der Anwendungs Einsichten.</span><span class="sxs-lookup"><span data-stu-id="3293f-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="3293f-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3293f-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3293f-124">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="3293f-124">-IsBuffered</span></span>
<span data-ttu-id="3293f-125">Gibt an, dass die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="3293f-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="3293f-126">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="3293f-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3293f-127">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="3293f-127">-LoggerId</span></span>
<span data-ttu-id="3293f-128">Gibt die ID der Protokollierung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3293f-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="3293f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3293f-129">-Name</span></span>
<span data-ttu-id="3293f-130">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="3293f-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3293f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3293f-131">-PassThru</span></span>
<span data-ttu-id="3293f-132">Gibt an, dass dieses Cmdlet die  **PsApiManagementLogger** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3293f-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3293f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3293f-133">CommonParameters</span></span>
<span data-ttu-id="3293f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3293f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3293f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3293f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3293f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3293f-136">INPUTS</span></span>

### <span data-ttu-id="3293f-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3293f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3293f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3293f-138">System.String</span></span>

### <span data-ttu-id="3293f-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="3293f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3293f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3293f-140">OUTPUTS</span></span>

### <span data-ttu-id="3293f-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3293f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="3293f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3293f-142">NOTES</span></span>

## <span data-ttu-id="3293f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3293f-143">RELATED LINKS</span></span>

[<span data-ttu-id="3293f-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3293f-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3293f-145">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3293f-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3293f-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3293f-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


