---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165405"
---
# Get-AzWebAppSSLBinding

## Synopsis
Ruft eine Azure Web App-Zertifikat SSL-Bindung ab.

## Syntax

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzWebAppSSLBinding** " Ruft eine SSL-Bindung (Secure Sockets Layer) für eine Azure Web App ab.
SSL-Bindungen werden verwendet, um eine Web-App mit einem hochgeladenen Zertifikat zu verknüpfen.
Web-Apps können an mehrere Zertifikate gebunden werden.

## Beispiele

### Beispiel 1: Abrufen von SSL-Bindungen für eine Web-App
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Dieser Befehl ruft die SSL-Bindungen für das Web App ContosoWebApp ab, das der Ressourcengruppe ContosoResourceGroup zugeordnet ist.

### Beispiel 2: Verwenden eines Objektverweises zum Abrufen von SSL-Bindungen für eine Web-App
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Die Befehle in diesem Beispiel erhalten auch die SSL-Bindungen für das Web App ContosoWebApp; in diesem Fall wird jedoch anstelle des Web App-namens und des Namens der zugeordneten Ressourcengruppe ein Objektverweis verwendet.
Dieser Objektverweis wird mit dem ersten Befehl im Beispiel erstellt, der mithilfe von **Get-AzWebApp** einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp erstellt.
Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.
Diese Variable und das Cmdlet " **Get-AzWebAppSSLBinding** " werden dann vom zweiten Befehl verwendet, um die SSL-Bindungen abzurufen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Name
Gibt den Namen der SSL-Bindung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.
Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Gibt einen Web App-Bereitstellungs Steckplatz an.
Verwenden Sie das Get-AzWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webbasierte
Gibt eine Web-App an.
Verwenden Sie das Get-AzWebApp-Cmdlet, um eine Web-App abzurufen.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Webbasierter
Gibt den Namen der Web-App an, von der dieses Cmdlet SSL-Bindungen erhält.
Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. webapps. Models. PSSite

## Ausgaben

### Microsoft. Azure. Management. Websites. Models. HostNameSslState

## Notizen

## Verwandte Links

[Neu – AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


