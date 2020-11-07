---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 103c5e75b433fcb585113e8ef6bc89aab1f82d7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848607"
---
# <span data-ttu-id="33fa9-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="33fa9-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="33fa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="33fa9-103">Ruft eine Azure Web App-Zertifikat SSL-Bindung ab.</span><span class="sxs-lookup"><span data-stu-id="33fa9-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33fa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33fa9-104">SYNTAX</span></span>

### <span data-ttu-id="33fa9-105">S1</span><span class="sxs-lookup"><span data-stu-id="33fa9-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33fa9-106">S2</span><span class="sxs-lookup"><span data-stu-id="33fa9-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33fa9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="33fa9-108">Das Cmdlet " **Get-AzureRmWebAppSSLBinding** " Ruft eine SSL-Bindung (Secure Sockets Layer) für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="33fa9-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="33fa9-109">SSL-Bindungen werden verwendet, um eine Web-App mit einem hochgeladenen Zertifikat zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="33fa9-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="33fa9-110">Web-Apps können an mehrere Zertifikate gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="33fa9-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="33fa9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33fa9-111">EXAMPLES</span></span>

### <span data-ttu-id="33fa9-112">Beispiel 1: Abrufen von SSL-Bindungen für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="33fa9-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="33fa9-113">Dieser Befehl ruft die SSL-Bindungen für das Web App ContosoWebApp ab, das der Ressourcengruppe ContosoResourceGroup zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="33fa9-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="33fa9-114">Beispiel 2: Verwenden eines Objektverweises zum Abrufen von SSL-Bindungen für eine Web-App</span><span class="sxs-lookup"><span data-stu-id="33fa9-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="33fa9-115">Die Befehle in diesem Beispiel erhalten auch die SSL-Bindungen für das Web App ContosoWebApp; in diesem Fall wird jedoch anstelle des Web App-namens und des Namens der zugeordneten Ressourcengruppe ein Objektverweis verwendet.</span><span class="sxs-lookup"><span data-stu-id="33fa9-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="33fa9-116">Dieser Objektverweis wird mit dem ersten Befehl im Beispiel erstellt, der mithilfe von **Get-AzureRmWebApp** einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="33fa9-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="33fa9-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="33fa9-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="33fa9-118">Diese Variable und das Cmdlet " **Get-AzureRmWebAppSSLBinding** " werden dann vom zweiten Befehl verwendet, um die SSL-Bindungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="33fa9-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="33fa9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="33fa9-119">PARAMETERS</span></span>

### <span data-ttu-id="33fa9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fa9-120">-DefaultProfile</span></span>
<span data-ttu-id="33fa9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33fa9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="33fa9-122">-Name</span></span>
<span data-ttu-id="33fa9-123">Gibt den Namen der SSL-Bindung an.</span><span class="sxs-lookup"><span data-stu-id="33fa9-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fa9-124">-ResourceGroupName</span></span>
<span data-ttu-id="33fa9-125">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="33fa9-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="33fa9-126">Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="33fa9-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="33fa9-127">-Slot</span></span>
<span data-ttu-id="33fa9-128">Gibt einen Web App-Bereitstellungs Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="33fa9-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="33fa9-129">Verwenden Sie das Get-AzureRMWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="33fa9-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-130">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="33fa9-130">-WebApp</span></span>
<span data-ttu-id="33fa9-131">Gibt eine Web-App an.</span><span class="sxs-lookup"><span data-stu-id="33fa9-131">Specifies a Web App.</span></span>
<span data-ttu-id="33fa9-132">Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="33fa9-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-133">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="33fa9-133">-WebAppName</span></span>
<span data-ttu-id="33fa9-134">Gibt den Namen der Web-App an, von der dieses Cmdlet SSL-Bindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="33fa9-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="33fa9-135">Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="33fa9-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fa9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fa9-136">CommonParameters</span></span>
<span data-ttu-id="33fa9-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33fa9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fa9-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fa9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fa9-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33fa9-139">INPUTS</span></span>

### <span data-ttu-id="33fa9-140">Website</span><span class="sxs-lookup"><span data-stu-id="33fa9-140">Site</span></span>
<span data-ttu-id="33fa9-141">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="33fa9-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="33fa9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33fa9-142">OUTPUTS</span></span>

## <span data-ttu-id="33fa9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="33fa9-143">NOTES</span></span>

## <span data-ttu-id="33fa9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33fa9-144">RELATED LINKS</span></span>

[<span data-ttu-id="33fa9-145">Neu – AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="33fa9-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="33fa9-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="33fa9-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="33fa9-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="33fa9-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


