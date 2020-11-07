---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662201"
---
# <span data-ttu-id="4b799-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4b799-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="4b799-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b799-102">SYNOPSIS</span></span>
<span data-ttu-id="4b799-103">Erstellt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="4b799-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b799-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b799-104">SYNTAX</span></span>

### <span data-ttu-id="4b799-105">EventHubLoggerSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b799-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b799-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="4b799-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b799-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b799-107">DESCRIPTION</span></span>
<span data-ttu-id="4b799-108">Das Cmdlet **New-AzureRmApiManagementLogger** erstellt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="4b799-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="4b799-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b799-109">EXAMPLES</span></span>

### <span data-ttu-id="4b799-110">Beispiel 1: Erstellen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="4b799-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="4b799-111">Dieser Befehl erstellt eine Protokollierung mit dem Namen ContosoSdkEventHub mithilfe der angegebenen Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4b799-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="4b799-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b799-112">PARAMETERS</span></span>

### <span data-ttu-id="4b799-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4b799-113">-ConnectionString</span></span>
<span data-ttu-id="4b799-114">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die mit den folgenden Schritten beginnt: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="4b799-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="4b799-115">Der Schlüssel mit den Sende rechten in der Verbindungszeichenfolge muss konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="4b799-115">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="4b799-116">-Context</span><span class="sxs-lookup"><span data-stu-id="4b799-116">-Context</span></span>
<span data-ttu-id="4b799-117">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b799-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4b799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b799-118">-DefaultProfile</span></span>
<span data-ttu-id="4b799-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b799-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b799-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b799-120">-Description</span></span>
<span data-ttu-id="4b799-121">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="4b799-121">Specifies a description.</span></span>

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

### <span data-ttu-id="4b799-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="4b799-122">-InstrumentationKey</span></span>
<span data-ttu-id="4b799-123">Instrumentations Schlüssel der Anwendungs Einsichten.</span><span class="sxs-lookup"><span data-stu-id="4b799-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="4b799-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4b799-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b799-125">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="4b799-125">-IsBuffered</span></span>
<span data-ttu-id="4b799-126">Gibt an, ob die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="4b799-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="4b799-127">Der Standardwert ist $true.</span><span class="sxs-lookup"><span data-stu-id="4b799-127">The default value is $True.</span></span>
<span data-ttu-id="4b799-128">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="4b799-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="4b799-129">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="4b799-129">-LoggerId</span></span>
<span data-ttu-id="4b799-130">Gibt eine ID für die Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="4b799-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="4b799-131">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="4b799-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="4b799-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4b799-132">-Name</span></span>
<span data-ttu-id="4b799-133">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="4b799-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="4b799-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b799-134">CommonParameters</span></span>
<span data-ttu-id="4b799-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b799-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b799-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b799-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b799-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b799-137">INPUTS</span></span>

### <span data-ttu-id="4b799-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b799-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b799-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4b799-139">System.String</span></span>

### <span data-ttu-id="4b799-140">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4b799-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4b799-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b799-141">OUTPUTS</span></span>

### <span data-ttu-id="4b799-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4b799-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="4b799-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b799-143">NOTES</span></span>

## <span data-ttu-id="4b799-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b799-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b799-145">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4b799-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="4b799-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4b799-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="4b799-147">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4b799-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


