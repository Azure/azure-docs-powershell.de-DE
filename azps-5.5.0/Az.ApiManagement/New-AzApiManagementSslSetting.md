---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176300"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
Erstellt eine Instanz von "PsApiManagementSslSetting".

## SYNTAX

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Hilfsbefehl zum Erstellen einer Instanz von "PsApiManagementSslSetting".
Dieser Befehl wird zusammen mit dem Befehl New-AzApiManagement verwendet.

## BEISPIELE

### Beispiel 1: Erstellen einer SSL-Einstellung zum Aktivieren von TLS 1.0 für Back-End und Frontend
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

Erstellen Sie eine neue Instanz von PsApiManagementSslSetting, um TLSv 1.0 sowohl im Frontend (zwischen Client und APIM) als auch im Back-End (zwischen APIM und Back-End) des ApiManagement Gateways zu aktivieren.

## PARAMETERS

### -Back-EndProtocol
Back-End-Sicherheitsprotokolleinstellungen. Dieser Parameter ist optional.
Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0

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

### -CipherSuite
Einstellungen der Ssl-Verschlüsselungssammlung in der angegebenen Reihenfolge. Dieser Parameter ist optional.
Die gültigen Einstellungen sind `TripleDes168` : "Tripe Des 168 aktivieren/deaktivieren"

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -FrontendProtocol
Einstellungen für Frontend Security-Protokolle. Dieser Parameter ist optional.
Die gültigen Protokolleinstellungen `Tls11` sind – Tls 1.1 `Tls10` – Tls 1.0 `Ssl30` – SSL 3.0


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

### -ServerProtocol
Serverprotokolleinstellungen wie Http2. Dieser Parameter ist optional.
Die gültigen Einstellungen sind `Http2` – Http 2.0 aktivieren

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzApiManagement](./New-AzApiManagement.md)

