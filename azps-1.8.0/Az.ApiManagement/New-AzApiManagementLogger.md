---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 3df5f6974cd955035c16972a5a7358aa44a30390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661876"
---
# <span data-ttu-id="dc71d-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dc71d-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="dc71d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc71d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc71d-103">Erstellt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="dc71d-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="dc71d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc71d-104">SYNTAX</span></span>

### <span data-ttu-id="dc71d-105">EventHubLoggerSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc71d-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc71d-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="dc71d-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc71d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc71d-107">DESCRIPTION</span></span>
<span data-ttu-id="dc71d-108">Das Cmdlet **New-AzApiManagementLogger** erstellt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="dc71d-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="dc71d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc71d-109">EXAMPLES</span></span>

### <span data-ttu-id="dc71d-110">Beispiel 1: Erstellen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="dc71d-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="dc71d-111">Dieser Befehl erstellt eine Protokollierung mit dem Namen ContosoSdkEventHub mithilfe der angegebenen Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dc71d-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="dc71d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc71d-112">PARAMETERS</span></span>

### <span data-ttu-id="dc71d-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="dc71d-113">-ConnectionString</span></span>
<span data-ttu-id="dc71d-114">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die mit den folgenden Schritten beginnt: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="dc71d-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="dc71d-115">Der Schlüssel mit den Sende rechten in der Verbindungszeichenfolge muss konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="dc71d-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc71d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="dc71d-116">-Context</span></span>
<span data-ttu-id="dc71d-117">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="dc71d-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dc71d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc71d-118">-DefaultProfile</span></span>
<span data-ttu-id="dc71d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc71d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc71d-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc71d-120">-Description</span></span>
<span data-ttu-id="dc71d-121">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="dc71d-121">Specifies a description.</span></span>

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

### <span data-ttu-id="dc71d-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="dc71d-122">-InstrumentationKey</span></span>
<span data-ttu-id="dc71d-123">Instrumentations Schlüssel der Anwendungs Einsichten.</span><span class="sxs-lookup"><span data-stu-id="dc71d-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="dc71d-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dc71d-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc71d-125">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="dc71d-125">-IsBuffered</span></span>
<span data-ttu-id="dc71d-126">Gibt an, ob die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="dc71d-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="dc71d-127">Der Standardwert ist $true.</span><span class="sxs-lookup"><span data-stu-id="dc71d-127">The default value is $True.</span></span>
<span data-ttu-id="dc71d-128">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="dc71d-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc71d-129">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="dc71d-129">-LoggerId</span></span>
<span data-ttu-id="dc71d-130">Gibt eine ID für die Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="dc71d-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="dc71d-131">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="dc71d-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="dc71d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="dc71d-132">-Name</span></span>
<span data-ttu-id="dc71d-133">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="dc71d-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc71d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc71d-134">CommonParameters</span></span>
<span data-ttu-id="dc71d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc71d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc71d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc71d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc71d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc71d-137">INPUTS</span></span>

### <span data-ttu-id="dc71d-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc71d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc71d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc71d-139">System.String</span></span>

### <span data-ttu-id="dc71d-140">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc71d-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dc71d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc71d-141">OUTPUTS</span></span>

### <span data-ttu-id="dc71d-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dc71d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="dc71d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc71d-143">NOTES</span></span>

## <span data-ttu-id="dc71d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc71d-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc71d-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dc71d-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="dc71d-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dc71d-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="dc71d-147">Satz-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dc71d-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


