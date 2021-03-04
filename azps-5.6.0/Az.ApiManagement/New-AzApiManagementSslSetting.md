---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944333"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
Erstellt eine Instanz von PsApiManagementSslSetting

## SYNTAX

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Befehl "Hilfsbefehl", um eine Instanz von PsApiManagementSslSetting zu erstellen.
Dieser Befehl ist zusammen mit dem Befehl New-AzApiManagement zu verwenden.

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

## PARAMETER

### -Back-EndProtocol
Einstellungen für das Back-End-Sicherheitsprotokoll. Dieser Parameter ist optional.
Die gültigen Protokolleinstellungen `Tls11` sind - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0

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
Einstellungen für Ssl-Verschlüsselungssammlungen in der angegebenen Reihenfolge. Dieser Parameter ist optional.
Die gültigen Einstellungen sind `TripleDes168` : Aktivieren/Deaktivieren von Tripe Des 168

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
Die gültigen Protokolleinstellungen `Tls11` sind - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0


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
Die gültigen Einstellungen `Http2` sind – Aktivieren von Http 2.0

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings

## NOTIZEN

## VERWANDTE LINKS

[New-AzApiManagement](./New-AzApiManagement.md)

