---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 6ad32b3bd9bef4f4e684125b280db941da7a7b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004386"
---
# <span data-ttu-id="d644b-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d644b-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="d644b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d644b-102">SYNOPSIS</span></span>
<span data-ttu-id="d644b-103">Ändert eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="d644b-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="d644b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d644b-104">SYNTAX</span></span>

### <span data-ttu-id="d644b-105">EventHubLoggerSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d644b-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d644b-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="d644b-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d644b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d644b-107">DESCRIPTION</span></span>
<span data-ttu-id="d644b-108">Das Cmdlet " **festlegen-AzApiManagementLogger** " ändert die Einstellungen einer Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="d644b-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="d644b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d644b-109">EXAMPLES</span></span>

### <span data-ttu-id="d644b-110">Beispiel 1: Ändern der EventHub-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="d644b-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="d644b-111">Mit diesem Befehl wird eine Protokollierung geändert, die die ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="d644b-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="d644b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d644b-112">PARAMETERS</span></span>

### <span data-ttu-id="d644b-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d644b-113">-ConnectionString</span></span>
<span data-ttu-id="d644b-114">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die Sende Richtlinienrechte umfasst.</span><span class="sxs-lookup"><span data-stu-id="d644b-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="d644b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d644b-115">-Context</span></span>
<span data-ttu-id="d644b-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d644b-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d644b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d644b-117">-DefaultProfile</span></span>
<span data-ttu-id="d644b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d644b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d644b-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d644b-119">-Description</span></span>
<span data-ttu-id="d644b-120">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="d644b-120">Specifies a description.</span></span>

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

### <span data-ttu-id="d644b-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="d644b-121">-InstrumentationKey</span></span>
<span data-ttu-id="d644b-122">Instrumentations Schlüssel der Anwendungs Einsichten.</span><span class="sxs-lookup"><span data-stu-id="d644b-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="d644b-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d644b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="d644b-124">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="d644b-124">-IsBuffered</span></span>
<span data-ttu-id="d644b-125">Gibt an, dass die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="d644b-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="d644b-126">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="d644b-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="d644b-127">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="d644b-127">-LoggerId</span></span>
<span data-ttu-id="d644b-128">Gibt die ID der Protokollierung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d644b-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="d644b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d644b-129">-Name</span></span>
<span data-ttu-id="d644b-130">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="d644b-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="d644b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d644b-131">-PassThru</span></span>
<span data-ttu-id="d644b-132">Gibt an, dass dieses Cmdlet die  **PsApiManagementLogger** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d644b-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d644b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d644b-133">-Confirm</span></span>
<span data-ttu-id="d644b-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d644b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d644b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d644b-135">-WhatIf</span></span>
<span data-ttu-id="d644b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d644b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d644b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d644b-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d644b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d644b-138">CommonParameters</span></span>
<span data-ttu-id="d644b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d644b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d644b-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d644b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d644b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d644b-141">INPUTS</span></span>

### <span data-ttu-id="d644b-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d644b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d644b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d644b-143">System.String</span></span>

### <span data-ttu-id="d644b-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d644b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d644b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d644b-145">OUTPUTS</span></span>

### <span data-ttu-id="d644b-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d644b-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="d644b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d644b-147">NOTES</span></span>

## <span data-ttu-id="d644b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d644b-148">RELATED LINKS</span></span>

[<span data-ttu-id="d644b-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d644b-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="d644b-150">Neu – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d644b-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="d644b-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d644b-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


