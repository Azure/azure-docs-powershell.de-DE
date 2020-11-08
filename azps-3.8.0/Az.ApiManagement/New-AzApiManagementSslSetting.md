---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996911"
---
# <span data-ttu-id="46567-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="46567-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="46567-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46567-102">SYNOPSIS</span></span>
<span data-ttu-id="46567-103">Erstellt eine Instanz von PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="46567-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="46567-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46567-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46567-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46567-105">DESCRIPTION</span></span>
<span data-ttu-id="46567-106">Hilfsbefehl zum Erstellen einer Instanz von PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="46567-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="46567-107">Dieser Befehl ist mit New-AzApiManagement Befehl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="46567-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="46567-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46567-108">EXAMPLES</span></span>

### <span data-ttu-id="46567-109">Beispiel 1: Erstellen einer SSL-Einstellung zum Aktivieren von TLS 1,0 auf Back-End und Frontend</span><span class="sxs-lookup"><span data-stu-id="46567-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="46567-110">Erstellen Sie eine neue Instanz von PsApiManagementSslSetting, um TLSv 1,0 sowohl im Frontend (zwischen Client und APIM) als auch im Back-End (zwischen APIM und Back-End) des ApiManagement-Gateways zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="46567-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="46567-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46567-111">PARAMETERS</span></span>

### <span data-ttu-id="46567-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="46567-112">-BackendProtocol</span></span>
<span data-ttu-id="46567-113">Back-End-Sicherheitsprotokolleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="46567-113">Backend Security protocol settings.</span></span> <span data-ttu-id="46567-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="46567-114">This parameter is optional.</span></span>
<span data-ttu-id="46567-115">Die gültigen Protokolleinstellungen sind `Tls11` -TLS 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="46567-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46567-116">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="46567-116">-CipherSuite</span></span>
<span data-ttu-id="46567-117">Einstellungen für SSL-Verschlüsselungs Pakete in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="46567-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="46567-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="46567-118">This parameter is optional.</span></span>
<span data-ttu-id="46567-119">Die gültigen Einstellungen sind `TripleDes168` -Aktivieren/Deaktivieren von Kutteln des 168</span><span class="sxs-lookup"><span data-stu-id="46567-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46567-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46567-120">-DefaultProfile</span></span>
<span data-ttu-id="46567-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46567-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46567-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="46567-122">-FrontendProtocol</span></span>
<span data-ttu-id="46567-123">Einstellungen für das Frontend-Sicherheitsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="46567-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="46567-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="46567-124">This parameter is optional.</span></span>
<span data-ttu-id="46567-125">Die gültigen Protokolleinstellungen sind `Tls11` -TLS 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="46567-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46567-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="46567-126">-ServerProtocol</span></span>
<span data-ttu-id="46567-127">Server Protokolleinstellungen wie Http2.</span><span class="sxs-lookup"><span data-stu-id="46567-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="46567-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="46567-128">This parameter is optional.</span></span>
<span data-ttu-id="46567-129">Die gültigen Einstellungen sind `Http2` -enable http 2,0</span><span class="sxs-lookup"><span data-stu-id="46567-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46567-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46567-130">CommonParameters</span></span>
<span data-ttu-id="46567-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46567-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46567-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46567-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46567-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46567-133">INPUTS</span></span>

### <span data-ttu-id="46567-134">Keine</span><span class="sxs-lookup"><span data-stu-id="46567-134">None</span></span>

## <span data-ttu-id="46567-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46567-135">OUTPUTS</span></span>

### <span data-ttu-id="46567-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="46567-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="46567-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="46567-137">NOTES</span></span>

## <span data-ttu-id="46567-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46567-138">RELATED LINKS</span></span>

[<span data-ttu-id="46567-139">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="46567-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

